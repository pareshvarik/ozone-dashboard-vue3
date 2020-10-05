<template>
	<div class="row">
		
		 <div class="col-12">
			<card
				:title="table1.title"
				:subTitle="table1.subTitle"
			>
				<div
					slot="raw-content"
					class="table-responsive"
				>
					<paper-table
						:data="table1.data"
						:columns="table1.columns"
					>

					</paper-table>
				</div>
			</card> 
		</div>
		


		<div class="col-xl-4 col-lg-5 col-md-6">
			
		
			
			<!-- <user-card>

			</user-card>  -->
			<!-- <members-card>

        </members-card> -->
		</div>
		<!-- <div class="col-xl-8 col-lg-7 col-md-6">
			<edit-profile-form>

			</edit-profile-form>
		</div> -->
	</div>
</template>
<script>
import EditProfileForm from "./UserProfile/EditProfileForm.vue";
import UserCard from "./UserProfile/UserCard.vue";
import MembersCard from "./UserProfile/MembersCard.vue";
import { PaperTable } from "@/components";
const tableColumns = ["Id","FirstName","LastName", "Country"];
const tableData = [
	{
		id: 1,
		firstname: "Dakota ",
		lastname: "Rice",
		// salary: "$36.738",
		country: "Niger"
		// city: "Oud-Turnhout",
	},
	{
		id: 2,
		firstname: "Minerva Hooper",
		lastname: "Rice",
		// salary: "$23,789",
		country: "Curaçao"
		// city: "Sinaai-Waas",
	},
	{
		id: 3,
		firstname: "Sage Rodriguez",
		lastname: "Rice",
		// salary: "$56,142",
		country: "Netherlands"
		// city: "Baileux",
	},
	{
		id: 4,
		firstname: "Philip Chaney",
		lastname: "Rice",
		// salary: "$38,735",
		country: "Korea, South"
		// city: "Overland Park",
	},
	{
		id:5,
		firstname: "Doris Greene",
		lastname: "Rice",
		// salary: "$63,542",
		country: "Malawi"
		// city: "Feldkirchen in Kärnten",
	},
];
export default {
  components: {
    EditProfileForm,
    UserCard,
	MembersCard,
	PaperTable
  },
  data() {
		return {
			table1: {
				title: "Stripped Table",
				subTitle: "Here is a subtitle for this table",
				columns: [...tableColumns],
				data: [...tableData],
			},
			details: [
				{
					title: "id",
					subTitle: "Files",
				},
				{
					title: "firstname",
					subTitle: "Used",
				},
				{
					title: "24,6$",
					subTitle: "Spent",
				},
			],
		};
	},
};
</script>
<style>
</style>

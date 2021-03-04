---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/powershell/module/az.databox/get-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
ms.openlocfilehash: af406af487e03c429a21a99799083f67d0fabf53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913942"
---
# <span data-ttu-id="84298-101">Get-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="84298-101">Get-AzDataBoxJob</span></span>

## <span data-ttu-id="84298-102">簡介</span><span class="sxs-lookup"><span data-stu-id="84298-102">SYNOPSIS</span></span>
<span data-ttu-id="84298-103">獲得資料箱工作相關資訊</span><span class="sxs-lookup"><span data-stu-id="84298-103">Gets information about Databox Jobs</span></span>

## <span data-ttu-id="84298-104">語法</span><span class="sxs-lookup"><span data-stu-id="84298-104">SYNTAX</span></span>

### <span data-ttu-id="84298-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="84298-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxJob [-ResourceGroupName <String>] [-Completed] [-CompletedWithError] [-Cancelled] [-Aborted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84298-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="84298-106">GetByNameParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84298-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="84298-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84298-108">描述</span><span class="sxs-lookup"><span data-stu-id="84298-108">DESCRIPTION</span></span>
<span data-ttu-id="84298-109">**Get-AzDataBoxJobs** Cmdlet 會取得 Azure 訂閱中資料箱工作的資訊。</span><span class="sxs-lookup"><span data-stu-id="84298-109">The **Get-AzDataBoxJobs** cmdlet gets information about databox jobs in an Azure subscription.</span></span>
<span data-ttu-id="84298-110">如果您指定資源群組，此 Cmdlet 會獲得該資源群組下的所有資料箱工作。</span><span class="sxs-lookup"><span data-stu-id="84298-110">If you specify the Resource Group, this cmdlet gets all the databox jobs under that resource group.</span></span> <span data-ttu-id="84298-111">如果您指定工作名稱以及資源組名，此 Cmdlet 會獲得該特定資料箱工作的資訊。</span><span class="sxs-lookup"><span data-stu-id="84298-111">If you specify the Name of the job along with the resource group name, this cmdlet gets information about that specific databox job.</span></span>
<span data-ttu-id="84298-112">如果您未指定訂閱識別碼外的其他專案，此 Cmdlet 會獲得該訂閱下所有資料箱工作的資訊。</span><span class="sxs-lookup"><span data-stu-id="84298-112">If you do not specify anything other than subscription id, this cmdlet gets information about all of the databox jobs under that subscription.</span></span>

## <span data-ttu-id="84298-113">例子</span><span class="sxs-lookup"><span data-stu-id="84298-113">EXAMPLES</span></span>

### <span data-ttu-id="84298-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="84298-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxJob

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1
cleanbox                DataBox              Aborted             04-12-2018 16:07:41   westus               TestRg2
cleanbox-Clone          DataBox              Cancelled           25-04-2019 11:31:36   westus               TestRg2
.
.
.
```

<span data-ttu-id="84298-115">Get-AzDataBoxJob參數的情況下，會抓取訂閱下的所有資料箱工作</span><span class="sxs-lookup"><span data-stu-id="84298-115">Get-AzDataBoxJob without any parameter fetches all the databox jobs under the subscription</span></span>

### <span data-ttu-id="84298-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="84298-116">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1
.
.
.
```

<span data-ttu-id="84298-117">Get-AzDataBoxJob ResourceGroupName 參數時，會抓取指定資源群組下的所有資料箱工作</span><span class="sxs-lookup"><span data-stu-id="84298-117">Get-AzDataBoxJob with ResourceGroupName parameter fetches all the databox jobs under the specified resource group</span></span>

### <span data-ttu-id="84298-118">範例 3</span><span class="sxs-lookup"><span data-stu-id="84298-118">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1 -Name testtip2

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="84298-119">Get-AzDataBoxJob ResourceGroupName 和 Name 的指定專案會抓取該特定資料箱工作</span><span class="sxs-lookup"><span data-stu-id="84298-119">Get-AzDataBoxJob with ResourceGroupName and Name specified will fetch that specific databox job</span></span>

### <span data-ttu-id="84298-120">範例 4</span><span class="sxs-lookup"><span data-stu-id="84298-120">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/testtip2"

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="84298-121">Get-AzDataBoxJob ResourceId 的作業會抓取該特定資料箱工作</span><span class="sxs-lookup"><span data-stu-id="84298-121">Get-AzDataBoxJob with ResourceId specified will fetch that specific databox job</span></span>

## <span data-ttu-id="84298-122">參數</span><span class="sxs-lookup"><span data-stu-id="84298-122">PARAMETERS</span></span>

### <span data-ttu-id="84298-123">-已中止</span><span class="sxs-lookup"><span data-stu-id="84298-123">-Aborted</span></span>
<span data-ttu-id="84298-124">切換參數以抓取已中止的工作</span><span class="sxs-lookup"><span data-stu-id="84298-124">Switch Parameter to fetch Aborted jobs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84298-125">-已取消</span><span class="sxs-lookup"><span data-stu-id="84298-125">-Cancelled</span></span>
<span data-ttu-id="84298-126">切換參數以抓取已取消的工作</span><span class="sxs-lookup"><span data-stu-id="84298-126">Switch Parameter to fetch Cancelled jobs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84298-127">-已完成</span><span class="sxs-lookup"><span data-stu-id="84298-127">-Completed</span></span>
<span data-ttu-id="84298-128">切換參數以抓取已完成的工作</span><span class="sxs-lookup"><span data-stu-id="84298-128">Switch Parameter to fetch Completed jobs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84298-129">-CompletedWithError</span><span class="sxs-lookup"><span data-stu-id="84298-129">-CompletedWithError</span></span>
<span data-ttu-id="84298-130">切換參數以抓取有錯誤的工作</span><span class="sxs-lookup"><span data-stu-id="84298-130">Switch Parameter to fetch jobs completed with errors</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84298-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84298-131">-DefaultProfile</span></span>
<span data-ttu-id="84298-132">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="84298-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84298-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="84298-133">-Name</span></span>
<span data-ttu-id="84298-134">資料箱工作名稱</span><span class="sxs-lookup"><span data-stu-id="84298-134">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84298-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84298-135">-ResourceGroupName</span></span>
<span data-ttu-id="84298-136">資料箱工作資源組名</span><span class="sxs-lookup"><span data-stu-id="84298-136">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84298-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84298-137">-ResourceId</span></span>
<span data-ttu-id="84298-138">資料箱工作資源識別碼</span><span class="sxs-lookup"><span data-stu-id="84298-138">Databox Job Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84298-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84298-139">CommonParameters</span></span>
<span data-ttu-id="84298-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="84298-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84298-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84298-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84298-142">輸入</span><span class="sxs-lookup"><span data-stu-id="84298-142">INPUTS</span></span>

### <span data-ttu-id="84298-143">System.String</span><span class="sxs-lookup"><span data-stu-id="84298-143">System.String</span></span>

## <span data-ttu-id="84298-144">輸出</span><span class="sxs-lookup"><span data-stu-id="84298-144">OUTPUTS</span></span>

### <span data-ttu-id="84298-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="84298-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="84298-146">筆記</span><span class="sxs-lookup"><span data-stu-id="84298-146">NOTES</span></span>

## <span data-ttu-id="84298-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="84298-147">RELATED LINKS</span></span>

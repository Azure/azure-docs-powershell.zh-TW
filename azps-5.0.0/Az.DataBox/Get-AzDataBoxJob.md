---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
ms.openlocfilehash: 8669ee676f3f2be1f1a0064ed9fbbe88f3d113ee
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285374"
---
# <span data-ttu-id="12ed4-101">Get-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="12ed4-101">Get-AzDataBoxJob</span></span>

## <span data-ttu-id="12ed4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="12ed4-102">SYNOPSIS</span></span>
<span data-ttu-id="12ed4-103">取得 Databox 工作的相關資訊</span><span class="sxs-lookup"><span data-stu-id="12ed4-103">Gets information about Databox Jobs</span></span>

## <span data-ttu-id="12ed4-104">句法</span><span class="sxs-lookup"><span data-stu-id="12ed4-104">SYNTAX</span></span>

### <span data-ttu-id="12ed4-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="12ed4-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxJob [-ResourceGroupName <String>] [-Completed] [-CompletedWithError] [-Cancelled] [-Aborted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12ed4-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="12ed4-106">GetByNameParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12ed4-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="12ed4-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12ed4-108">說明</span><span class="sxs-lookup"><span data-stu-id="12ed4-108">DESCRIPTION</span></span>
<span data-ttu-id="12ed4-109">**AzDataBoxJobs** Cmdlet 會取得 Azure 訂閱中 databox 作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="12ed4-109">The **Get-AzDataBoxJobs** cmdlet gets information about databox jobs in an Azure subscription.</span></span>
<span data-ttu-id="12ed4-110">如果您指定 [資源] 群組，此 Cmdlet 會取得該資源群組下的所有 databox 作業。</span><span class="sxs-lookup"><span data-stu-id="12ed4-110">If you specify the Resource Group, this cmdlet gets all the databox jobs under that resource group.</span></span> <span data-ttu-id="12ed4-111">如果您指定作業的名稱與資源群組的名稱，此 Cmdlet 會取得該特定 databox 作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="12ed4-111">If you specify the Name of the job along with the resource group name, this cmdlet gets information about that specific databox job.</span></span>
<span data-ttu-id="12ed4-112">如果您沒有指定訂閱 id 以外的任何專案，這個 Cmdlet 會取得該訂閱下所有 databox 工作的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="12ed4-112">If you do not specify anything other than subscription id, this cmdlet gets information about all of the databox jobs under that subscription.</span></span>

## <span data-ttu-id="12ed4-113">示例</span><span class="sxs-lookup"><span data-stu-id="12ed4-113">EXAMPLES</span></span>

### <span data-ttu-id="12ed4-114">範例1</span><span class="sxs-lookup"><span data-stu-id="12ed4-114">Example 1</span></span>
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

<span data-ttu-id="12ed4-115">Get-AzDataBoxJob 沒有任何參數，就會提取訂閱下的所有 databox 工作</span><span class="sxs-lookup"><span data-stu-id="12ed4-115">Get-AzDataBoxJob without any parameter fetches all the databox jobs under the subscription</span></span>

### <span data-ttu-id="12ed4-116">範例2</span><span class="sxs-lookup"><span data-stu-id="12ed4-116">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1
.
.
.
```

<span data-ttu-id="12ed4-117">使用 ResourceGroupName 參數的 Get-AzDataBoxJob 會在指定的資源群組下取得所有 databox 作業</span><span class="sxs-lookup"><span data-stu-id="12ed4-117">Get-AzDataBoxJob with ResourceGroupName parameter fetches all the databox jobs under the specified resource group</span></span>

### <span data-ttu-id="12ed4-118">範例3</span><span class="sxs-lookup"><span data-stu-id="12ed4-118">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1 -Name testtip2

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="12ed4-119">使用 ResourceGroupName 和名稱指定的 Get-AzDataBoxJob，將會取得特定 databox 作業</span><span class="sxs-lookup"><span data-stu-id="12ed4-119">Get-AzDataBoxJob with ResourceGroupName and Name specified will fetch that specific databox job</span></span>

### <span data-ttu-id="12ed4-120">範例4</span><span class="sxs-lookup"><span data-stu-id="12ed4-120">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/testtip2"

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="12ed4-121">已指定 ResourceId 的 Get-AzDataBoxJob 將會提取特定的 databox 工作</span><span class="sxs-lookup"><span data-stu-id="12ed4-121">Get-AzDataBoxJob with ResourceId specified will fetch that specific databox job</span></span>

## <span data-ttu-id="12ed4-122">參數</span><span class="sxs-lookup"><span data-stu-id="12ed4-122">PARAMETERS</span></span>

### <span data-ttu-id="12ed4-123">-已中止</span><span class="sxs-lookup"><span data-stu-id="12ed4-123">-Aborted</span></span>
<span data-ttu-id="12ed4-124">切換參數以提取中止的作業</span><span class="sxs-lookup"><span data-stu-id="12ed4-124">Switch Parameter to fetch Aborted jobs</span></span>

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

### <span data-ttu-id="12ed4-125">-已取消</span><span class="sxs-lookup"><span data-stu-id="12ed4-125">-Cancelled</span></span>
<span data-ttu-id="12ed4-126">切換參數以取得已取消的作業</span><span class="sxs-lookup"><span data-stu-id="12ed4-126">Switch Parameter to fetch Cancelled jobs</span></span>

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

### <span data-ttu-id="12ed4-127">-已完成</span><span class="sxs-lookup"><span data-stu-id="12ed4-127">-Completed</span></span>
<span data-ttu-id="12ed4-128">切換參數以取得完成的作業</span><span class="sxs-lookup"><span data-stu-id="12ed4-128">Switch Parameter to fetch Completed jobs</span></span>

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

### <span data-ttu-id="12ed4-129">-CompletedWithError</span><span class="sxs-lookup"><span data-stu-id="12ed4-129">-CompletedWithError</span></span>
<span data-ttu-id="12ed4-130">已完成但有錯誤的參數切換至回遷作業</span><span class="sxs-lookup"><span data-stu-id="12ed4-130">Switch Parameter to fetch jobs completed with errors</span></span>

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

### <span data-ttu-id="12ed4-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12ed4-131">-DefaultProfile</span></span>
<span data-ttu-id="12ed4-132">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="12ed4-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12ed4-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="12ed4-133">-Name</span></span>
<span data-ttu-id="12ed4-134">Databox 工作名稱</span><span class="sxs-lookup"><span data-stu-id="12ed4-134">Databox Job Name</span></span>

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

### <span data-ttu-id="12ed4-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12ed4-135">-ResourceGroupName</span></span>
<span data-ttu-id="12ed4-136">Databox 工作資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="12ed4-136">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="12ed4-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12ed4-137">-ResourceId</span></span>
<span data-ttu-id="12ed4-138">Databox 工作資源識別碼</span><span class="sxs-lookup"><span data-stu-id="12ed4-138">Databox Job Resource Id</span></span>

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

### <span data-ttu-id="12ed4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12ed4-139">CommonParameters</span></span>
<span data-ttu-id="12ed4-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="12ed4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12ed4-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="12ed4-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12ed4-142">輸入</span><span class="sxs-lookup"><span data-stu-id="12ed4-142">INPUTS</span></span>

### <span data-ttu-id="12ed4-143">System.object</span><span class="sxs-lookup"><span data-stu-id="12ed4-143">System.String</span></span>

## <span data-ttu-id="12ed4-144">輸出</span><span class="sxs-lookup"><span data-stu-id="12ed4-144">OUTPUTS</span></span>

### <span data-ttu-id="12ed4-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="12ed4-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="12ed4-146">筆記</span><span class="sxs-lookup"><span data-stu-id="12ed4-146">NOTES</span></span>

## <span data-ttu-id="12ed4-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="12ed4-147">RELATED LINKS</span></span>

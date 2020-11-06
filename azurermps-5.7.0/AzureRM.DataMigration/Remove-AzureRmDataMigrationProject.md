---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/remove-azurermdatamigrationproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationProject.md
ms.openlocfilehash: 8ec046df13302ece90e57bcb722816f2019ff2e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455419"
---
# <span data-ttu-id="a8fac-101">Remove-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="a8fac-101">Remove-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="a8fac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a8fac-102">SYNOPSIS</span></span>
<span data-ttu-id="a8fac-103">從 Azure 移除 Azure 資料庫移轉服務專案。</span><span class="sxs-lookup"><span data-stu-id="a8fac-103">Removes an Azure Database Migration Service project from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8fac-104">句法</span><span class="sxs-lookup"><span data-stu-id="a8fac-104">SYNTAX</span></span>

### <span data-ttu-id="a8fac-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a8fac-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Name <String> [-Force]
 [-DeleteRunningTask] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a8fac-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8fac-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationProject [-InputObject] <PSProject> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a8fac-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8fac-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationProject [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a8fac-108">說明</span><span class="sxs-lookup"><span data-stu-id="a8fac-108">DESCRIPTION</span></span>
<span data-ttu-id="a8fac-109">Remove-AzureRmDataMigrationProject Cmdlet 會從 Azure 中移除 Azure 資料庫移轉服務專案。</span><span class="sxs-lookup"><span data-stu-id="a8fac-109">The Remove-AzureRmDataMigrationProject cmdlet removes an Azure Database Migration Service project from Azure.</span></span> <span data-ttu-id="a8fac-110">提供 DeleteRunningTask 參數時，會移除與所移除專案相關聯的所有 Azure 資料庫移轉服務任務。</span><span class="sxs-lookup"><span data-stu-id="a8fac-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the project that is being removed.</span></span> 

## <span data-ttu-id="a8fac-111">示例</span><span class="sxs-lookup"><span data-stu-id="a8fac-111">EXAMPLES</span></span>

### <span data-ttu-id="a8fac-112">範例1</span><span class="sxs-lookup"><span data-stu-id="a8fac-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationProject -ResourceGroupName myResourceGroup -ServiceName myDMService -ProjectName myDMProject
```

<span data-ttu-id="a8fac-113">上述範例會根據 name 作為輸入參數，從 Azure 中移除名為 myDMProject 的 Azure 資料庫移轉服務專案</span><span class="sxs-lookup"><span data-stu-id="a8fac-113">The above example removes the Azure Database Migration Service project called myDMProject from Azure based on name as input parameter</span></span>

### <span data-ttu-id="a8fac-114">範例2</span><span class="sxs-lookup"><span data-stu-id="a8fac-114">Example 2</span></span>
```
PS C:\> Remove-AzureRmDataMigrationProject -InputObject $myDMSProject
```

<span data-ttu-id="a8fac-115">上述範例會根據 PSProject 物件做為輸入參數，移除 Azure 資料庫移轉服務專案。</span><span class="sxs-lookup"><span data-stu-id="a8fac-115">The above example removes the Azure Database Migration Service project based on PSProject object as input parameter.</span></span>

## <span data-ttu-id="a8fac-116">參數</span><span class="sxs-lookup"><span data-stu-id="a8fac-116">PARAMETERS</span></span>

### <span data-ttu-id="a8fac-117">-確認</span><span class="sxs-lookup"><span data-stu-id="a8fac-117">-Confirm</span></span>
<span data-ttu-id="a8fac-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a8fac-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8fac-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8fac-119">-DefaultProfile</span></span>
<span data-ttu-id="a8fac-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a8fac-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8fac-121">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="a8fac-121">-DeleteRunningTask</span></span>
<span data-ttu-id="a8fac-122">刪除任何執行中的任務</span><span class="sxs-lookup"><span data-stu-id="a8fac-122">Delete any running task</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8fac-123">-Force</span><span class="sxs-lookup"><span data-stu-id="a8fac-123">-Force</span></span>
<span data-ttu-id="a8fac-124">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="a8fac-124">Skip confirmation message for performing the action</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8fac-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8fac-125">-InputObject</span></span>
<span data-ttu-id="a8fac-126">PSProject 物件。</span><span class="sxs-lookup"><span data-stu-id="a8fac-126">PSProject Object.</span></span>

```yaml
Type: PSProject
Parameter Sets: ComponentObjectParameterSet
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8fac-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="a8fac-127">-Name</span></span>
<span data-ttu-id="a8fac-128">專案名稱。</span><span class="sxs-lookup"><span data-stu-id="a8fac-128">The name of the project.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8fac-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8fac-129">-PassThru</span></span>
<span data-ttu-id="a8fac-130">會傳回 true/false。</span><span class="sxs-lookup"><span data-stu-id="a8fac-130">Returns an true/false.</span></span>
<span data-ttu-id="a8fac-131">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="a8fac-131">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8fac-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8fac-132">-ResourceGroupName</span></span>
<span data-ttu-id="a8fac-133">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8fac-133">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8fac-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8fac-134">-ResourceId</span></span>
<span data-ttu-id="a8fac-135">[專案資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="a8fac-135">Project Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8fac-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a8fac-136">-ServiceName</span></span>
<span data-ttu-id="a8fac-137">資料移轉服務名稱。</span><span class="sxs-lookup"><span data-stu-id="a8fac-137">Data Migration Service Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8fac-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8fac-138">-WhatIf</span></span>
<span data-ttu-id="a8fac-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a8fac-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8fac-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a8fac-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="a8fac-141">輸入</span><span class="sxs-lookup"><span data-stu-id="a8fac-141">INPUTS</span></span>

### <span data-ttu-id="a8fac-142">PSProject 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="a8fac-142">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>
<span data-ttu-id="a8fac-143">System.object</span><span class="sxs-lookup"><span data-stu-id="a8fac-143">System.String</span></span>


## <span data-ttu-id="a8fac-144">輸出</span><span class="sxs-lookup"><span data-stu-id="a8fac-144">OUTPUTS</span></span>

### <span data-ttu-id="a8fac-145">System.object</span><span class="sxs-lookup"><span data-stu-id="a8fac-145">System.Boolean</span></span>


## <span data-ttu-id="a8fac-146">筆記</span><span class="sxs-lookup"><span data-stu-id="a8fac-146">NOTES</span></span>

## <span data-ttu-id="a8fac-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="a8fac-147">RELATED LINKS</span></span>


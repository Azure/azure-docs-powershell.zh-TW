---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/remove-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Remove-AzureRmDataMigrationService.md
ms.openlocfilehash: dde0044642f81c098358cd86cabe8c066240a215
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451519"
---
# <span data-ttu-id="9d635-101">Remove-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="9d635-101">Remove-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="9d635-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9d635-102">SYNOPSIS</span></span>
<span data-ttu-id="9d635-103">從 Azure 移除 Azure 資料庫移轉服務的實例。</span><span class="sxs-lookup"><span data-stu-id="9d635-103">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d635-104">句法</span><span class="sxs-lookup"><span data-stu-id="9d635-104">SYNTAX</span></span>

### <span data-ttu-id="9d635-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9d635-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="9d635-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d635-106">ComponentObjectParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-Force] [-DeleteRunningTask]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="9d635-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d635-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDataMigrationService [-ResourceId] <String> [-Force] [-DeleteRunningTask] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="9d635-108">說明</span><span class="sxs-lookup"><span data-stu-id="9d635-108">DESCRIPTION</span></span>
<span data-ttu-id="9d635-109">Remove-AzureRmDataMigrationService Cmdlet 會從 Azure 中移除 Azure 資料庫移轉服務的實例。</span><span class="sxs-lookup"><span data-stu-id="9d635-109">The Remove-AzureRmDataMigrationService cmdlet removes an instance of the Azure Database Migration Service from Azure.</span></span> <span data-ttu-id="9d635-110">提供 DeleteRunningTask 參數會移除與移除之服務相關聯的所有 Azure 資料庫移轉服務工作。</span><span class="sxs-lookup"><span data-stu-id="9d635-110">Supplying the DeleteRunningTask parameter removes all of the Azure Database Migration Service tasks associated with the service that is being removed.</span></span> 

## <span data-ttu-id="9d635-111">示例</span><span class="sxs-lookup"><span data-stu-id="9d635-111">EXAMPLES</span></span>

### <span data-ttu-id="9d635-112">範例1</span><span class="sxs-lookup"><span data-stu-id="9d635-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup –ServiceName TestService
```

<span data-ttu-id="9d635-113">上述範例會移除名為 [MyResourceGroup] 的 Azure 資源群組中包含的名為 TestService 的 Azure 資料庫移轉服務實例。</span><span class="sxs-lookup"><span data-stu-id="9d635-113">The above example removes an instance of the Azure Database Migration Service named TestService that is contained in an Azure Resource Group named MyResourceGroup.</span></span>

## <span data-ttu-id="9d635-114">參數</span><span class="sxs-lookup"><span data-stu-id="9d635-114">PARAMETERS</span></span>

### <span data-ttu-id="9d635-115">-確認</span><span class="sxs-lookup"><span data-stu-id="9d635-115">-Confirm</span></span>
<span data-ttu-id="9d635-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9d635-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d635-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d635-117">-DefaultProfile</span></span>
<span data-ttu-id="9d635-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d635-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d635-119">-DeleteRunningTask</span><span class="sxs-lookup"><span data-stu-id="9d635-119">-DeleteRunningTask</span></span>
<span data-ttu-id="9d635-120">刪除任何執行中的任務</span><span class="sxs-lookup"><span data-stu-id="9d635-120">Delete any running task</span></span>

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

### <span data-ttu-id="9d635-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9d635-121">-Force</span></span>
<span data-ttu-id="9d635-122">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="9d635-122">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="9d635-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d635-123">-InputObject</span></span>
<span data-ttu-id="9d635-124">PSDataMigrationService 物件。</span><span class="sxs-lookup"><span data-stu-id="9d635-124">PSDataMigrationService Object.</span></span>

```yaml
Type: PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d635-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="9d635-125">-Name</span></span>
<span data-ttu-id="9d635-126">資料移轉服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="9d635-126">The name of the Data Migration Service.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d635-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d635-127">-PassThru</span></span>
<span data-ttu-id="9d635-128">會傳回 true/false。</span><span class="sxs-lookup"><span data-stu-id="9d635-128">Returns an true/false.</span></span>
<span data-ttu-id="9d635-129">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="9d635-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9d635-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d635-130">-ResourceGroupName</span></span>
<span data-ttu-id="9d635-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9d635-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="9d635-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d635-132">-ResourceId</span></span>
<span data-ttu-id="9d635-133">DataMigrationService 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9d635-133">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="9d635-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d635-134">-WhatIf</span></span>
<span data-ttu-id="9d635-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9d635-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d635-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9d635-136">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="9d635-137">輸入</span><span class="sxs-lookup"><span data-stu-id="9d635-137">INPUTS</span></span>

### <span data-ttu-id="9d635-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="9d635-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="9d635-139">System.object</span><span class="sxs-lookup"><span data-stu-id="9d635-139">System.String</span></span>


## <span data-ttu-id="9d635-140">輸出</span><span class="sxs-lookup"><span data-stu-id="9d635-140">OUTPUTS</span></span>

### <span data-ttu-id="9d635-141">System.object</span><span class="sxs-lookup"><span data-stu-id="9d635-141">System.Boolean</span></span>


## <span data-ttu-id="9d635-142">筆記</span><span class="sxs-lookup"><span data-stu-id="9d635-142">NOTES</span></span>

## <span data-ttu-id="9d635-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="9d635-143">RELATED LINKS</span></span>



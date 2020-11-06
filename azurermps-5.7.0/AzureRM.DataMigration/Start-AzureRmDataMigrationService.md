---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/start-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Start-AzureRmDataMigrationService.md
ms.openlocfilehash: 03f07eaac1dbf616c78d1ca39561945b2a844b48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444552"
---
# <span data-ttu-id="8c54b-101">Start-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="8c54b-101">Start-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="8c54b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c54b-102">SYNOPSIS</span></span>
<span data-ttu-id="8c54b-103">在已停止的狀態中啟動 Azure Database 遷移服務的實例。</span><span class="sxs-lookup"><span data-stu-id="8c54b-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c54b-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c54b-104">SYNTAX</span></span>

### <span data-ttu-id="8c54b-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8c54b-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="8c54b-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c54b-106">ComponentObjectParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="8c54b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c54b-107">ResourceIdParameterSet</span></span>
```
Start-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="8c54b-108">說明</span><span class="sxs-lookup"><span data-stu-id="8c54b-108">DESCRIPTION</span></span>
<span data-ttu-id="8c54b-109">Start-AzureRmDataMigrationService Cmdlet 會在停止狀態中啟動 Azure Database 遷移服務的實例。</span><span class="sxs-lookup"><span data-stu-id="8c54b-109">The Start-AzureRmDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="8c54b-110">示例</span><span class="sxs-lookup"><span data-stu-id="8c54b-110">EXAMPLES</span></span>

### <span data-ttu-id="8c54b-111">範例1</span><span class="sxs-lookup"><span data-stu-id="8c54b-111">Example 1</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup –ServiceName TestService
```

<span data-ttu-id="8c54b-112">上述範例會根據以輸入的服務名稱，在停止狀態中啟動名為 Test 服務的 Azure 資料庫移轉服務實例</span><span class="sxs-lookup"><span data-stu-id="8c54b-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="8c54b-113">範例2</span><span class="sxs-lookup"><span data-stu-id="8c54b-113">Example 2</span></span>
```
PS C:\> Start-AzureRmDataMigrationService -InputObject $TestService
```

<span data-ttu-id="8c54b-114">上述範例會根據以輸入參數傳入的 PSDataMigrationService 來啟動 Azure Database 遷移服務實例</span><span class="sxs-lookup"><span data-stu-id="8c54b-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="8c54b-115">參數</span><span class="sxs-lookup"><span data-stu-id="8c54b-115">PARAMETERS</span></span>

### <span data-ttu-id="8c54b-116">-確認</span><span class="sxs-lookup"><span data-stu-id="8c54b-116">-Confirm</span></span>
<span data-ttu-id="8c54b-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8c54b-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c54b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c54b-118">-DefaultProfile</span></span>
<span data-ttu-id="8c54b-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8c54b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c54b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c54b-120">-InputObject</span></span>
<span data-ttu-id="8c54b-121">PSDataMigrationService 物件。</span><span class="sxs-lookup"><span data-stu-id="8c54b-121">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="8c54b-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="8c54b-122">-Name</span></span>
<span data-ttu-id="8c54b-123">資料移轉服務名稱。</span><span class="sxs-lookup"><span data-stu-id="8c54b-123">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="8c54b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c54b-124">-PassThru</span></span>
<span data-ttu-id="8c54b-125">會傳回 true/false。</span><span class="sxs-lookup"><span data-stu-id="8c54b-125">Returns an true/false.</span></span>
<span data-ttu-id="8c54b-126">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="8c54b-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8c54b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c54b-127">-ResourceGroupName</span></span>
<span data-ttu-id="8c54b-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c54b-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="8c54b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c54b-129">-ResourceId</span></span>
<span data-ttu-id="8c54b-130">DataMigrationService 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8c54b-130">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="8c54b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c54b-131">-WhatIf</span></span>
<span data-ttu-id="8c54b-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8c54b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c54b-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c54b-133">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="8c54b-134">輸入</span><span class="sxs-lookup"><span data-stu-id="8c54b-134">INPUTS</span></span>

### <span data-ttu-id="8c54b-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="8c54b-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="8c54b-136">System.object</span><span class="sxs-lookup"><span data-stu-id="8c54b-136">System.String</span></span>


## <span data-ttu-id="8c54b-137">輸出</span><span class="sxs-lookup"><span data-stu-id="8c54b-137">OUTPUTS</span></span>

### <span data-ttu-id="8c54b-138">System.object</span><span class="sxs-lookup"><span data-stu-id="8c54b-138">System.Boolean</span></span>


## <span data-ttu-id="8c54b-139">筆記</span><span class="sxs-lookup"><span data-stu-id="8c54b-139">NOTES</span></span>

## <span data-ttu-id="8c54b-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c54b-140">RELATED LINKS</span></span>



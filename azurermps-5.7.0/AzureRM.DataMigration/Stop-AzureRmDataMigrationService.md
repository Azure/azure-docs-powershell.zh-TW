---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/stop-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
ms.openlocfilehash: 9a3028e019d3873105df079b67652f2157137ce2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457179"
---
# <span data-ttu-id="cda69-101">Stop-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="cda69-101">Stop-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="cda69-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cda69-102">SYNOPSIS</span></span>
<span data-ttu-id="cda69-103">停止處於執行中狀態的 Azure 資料庫移轉服務實例。</span><span class="sxs-lookup"><span data-stu-id="cda69-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cda69-104">句法</span><span class="sxs-lookup"><span data-stu-id="cda69-104">SYNTAX</span></span>

### <span data-ttu-id="cda69-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="cda69-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="cda69-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cda69-106">ComponentObjectParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="cda69-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cda69-107">ResourceIdParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="cda69-108">說明</span><span class="sxs-lookup"><span data-stu-id="cda69-108">DESCRIPTION</span></span>
<span data-ttu-id="cda69-109">Stop-AzureRmDataMigrationService Cmdlet 會停止處於執行中狀態的 Azure 資料庫移轉服務實例。</span><span class="sxs-lookup"><span data-stu-id="cda69-109">The Stop-AzureRmDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="cda69-110">示例</span><span class="sxs-lookup"><span data-stu-id="cda69-110">EXAMPLES</span></span>

### <span data-ttu-id="cda69-111">範例1</span><span class="sxs-lookup"><span data-stu-id="cda69-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup –ServiceName TestService

```
<span data-ttu-id="cda69-112">上述範例會根據以輸入參數傳入的服務名稱來停止名為 TestService 的 Azure Database 遷移服務實例</span><span class="sxs-lookup"><span data-stu-id="cda69-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="cda69-113">範例2</span><span class="sxs-lookup"><span data-stu-id="cda69-113">Example 2</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -InputObject $TestService

```
<span data-ttu-id="cda69-114">上述範例會根據傳遞為輸入參數的 PSDataMigrationService 物件，來停止 Azure Database 遷移服務的實例。</span><span class="sxs-lookup"><span data-stu-id="cda69-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>



## <span data-ttu-id="cda69-115">參數</span><span class="sxs-lookup"><span data-stu-id="cda69-115">PARAMETERS</span></span>

### <span data-ttu-id="cda69-116">-確認</span><span class="sxs-lookup"><span data-stu-id="cda69-116">-Confirm</span></span>
<span data-ttu-id="cda69-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cda69-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cda69-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cda69-118">-DefaultProfile</span></span>
<span data-ttu-id="cda69-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cda69-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cda69-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cda69-120">-InputObject</span></span>
<span data-ttu-id="cda69-121">PSDataMigrationService 物件。</span><span class="sxs-lookup"><span data-stu-id="cda69-121">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="cda69-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="cda69-122">-Name</span></span>
<span data-ttu-id="cda69-123">資料移轉服務名稱。</span><span class="sxs-lookup"><span data-stu-id="cda69-123">Data Migration Service Name.</span></span>

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

### <span data-ttu-id="cda69-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cda69-124">-PassThru</span></span>
<span data-ttu-id="cda69-125">會傳回 true/false。</span><span class="sxs-lookup"><span data-stu-id="cda69-125">Returns an true/false.</span></span>
<span data-ttu-id="cda69-126">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="cda69-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cda69-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cda69-127">-ResourceGroupName</span></span>
<span data-ttu-id="cda69-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cda69-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="cda69-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cda69-129">-ResourceId</span></span>
<span data-ttu-id="cda69-130">DataMigrationService 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="cda69-130">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="cda69-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cda69-131">-WhatIf</span></span>
<span data-ttu-id="cda69-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cda69-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cda69-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cda69-133">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="cda69-134">輸入</span><span class="sxs-lookup"><span data-stu-id="cda69-134">INPUTS</span></span>

### <span data-ttu-id="cda69-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="cda69-135">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="cda69-136">System.object</span><span class="sxs-lookup"><span data-stu-id="cda69-136">System.String</span></span>


## <span data-ttu-id="cda69-137">輸出</span><span class="sxs-lookup"><span data-stu-id="cda69-137">OUTPUTS</span></span>

### <span data-ttu-id="cda69-138">System.object</span><span class="sxs-lookup"><span data-stu-id="cda69-138">System.Boolean</span></span>


## <span data-ttu-id="cda69-139">筆記</span><span class="sxs-lookup"><span data-stu-id="cda69-139">NOTES</span></span>

## <span data-ttu-id="cda69-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="cda69-140">RELATED LINKS</span></span>


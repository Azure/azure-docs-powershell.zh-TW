---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Stop-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
ms.openlocfilehash: 59ec77f0c6e3a2f9389931e12ecbce155fe970bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448448"
---
# <span data-ttu-id="efb20-101">Stop-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="efb20-101">Stop-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="efb20-102">摘要</span><span class="sxs-lookup"><span data-stu-id="efb20-102">SYNOPSIS</span></span>
<span data-ttu-id="efb20-103">停止處於執行中狀態的 Azure 資料庫移轉服務實例。</span><span class="sxs-lookup"><span data-stu-id="efb20-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efb20-104">句法</span><span class="sxs-lookup"><span data-stu-id="efb20-104">SYNTAX</span></span>

### <span data-ttu-id="efb20-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="efb20-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efb20-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="efb20-106">ComponentObjectParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efb20-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="efb20-107">ResourceIdParameterSet</span></span>
```
Stop-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efb20-108">說明</span><span class="sxs-lookup"><span data-stu-id="efb20-108">DESCRIPTION</span></span>
<span data-ttu-id="efb20-109">Stop-AzureRmDataMigrationService Cmdlet 會停止處於執行中狀態的 Azure 資料庫移轉服務實例。</span><span class="sxs-lookup"><span data-stu-id="efb20-109">The Stop-AzureRmDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="efb20-110">示例</span><span class="sxs-lookup"><span data-stu-id="efb20-110">EXAMPLES</span></span>

### <span data-ttu-id="efb20-111">範例1</span><span class="sxs-lookup"><span data-stu-id="efb20-111">Example 1</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="efb20-112">上述範例會根據以輸入參數傳入的服務名稱來停止名為 TestService 的 Azure Database 遷移服務實例</span><span class="sxs-lookup"><span data-stu-id="efb20-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="efb20-113">範例2</span><span class="sxs-lookup"><span data-stu-id="efb20-113">Example 2</span></span>
```
PS C:\> Stop-AzureRmDataMigrationService -InputObject $TestService
```

<span data-ttu-id="efb20-114">上述範例會根據傳遞為輸入參數的 PSDataMigrationService 物件，來停止 Azure Database 遷移服務的實例。</span><span class="sxs-lookup"><span data-stu-id="efb20-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>

## <span data-ttu-id="efb20-115">參數</span><span class="sxs-lookup"><span data-stu-id="efb20-115">PARAMETERS</span></span>

### <span data-ttu-id="efb20-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efb20-116">-DefaultProfile</span></span>
<span data-ttu-id="efb20-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="efb20-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efb20-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efb20-118">-InputObject</span></span>
<span data-ttu-id="efb20-119">PSDataMigrationService 物件。</span><span class="sxs-lookup"><span data-stu-id="efb20-119">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efb20-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="efb20-120">-Name</span></span>
<span data-ttu-id="efb20-121">資料庫移轉服務名稱。</span><span class="sxs-lookup"><span data-stu-id="efb20-121">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efb20-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="efb20-122">-PassThru</span></span>
<span data-ttu-id="efb20-123">會傳回 true/false。</span><span class="sxs-lookup"><span data-stu-id="efb20-123">Returns an true/false.</span></span>
<span data-ttu-id="efb20-124">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="efb20-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efb20-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efb20-125">-ResourceGroupName</span></span>
<span data-ttu-id="efb20-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="efb20-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efb20-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="efb20-127">-ResourceId</span></span>
<span data-ttu-id="efb20-128">DataMigrationService 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="efb20-128">DataMigrationService Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efb20-129">-確認</span><span class="sxs-lookup"><span data-stu-id="efb20-129">-Confirm</span></span>
<span data-ttu-id="efb20-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="efb20-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efb20-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efb20-131">-WhatIf</span></span>
<span data-ttu-id="efb20-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="efb20-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efb20-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="efb20-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efb20-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efb20-134">CommonParameters</span></span>
<span data-ttu-id="efb20-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="efb20-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efb20-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="efb20-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efb20-137">輸入</span><span class="sxs-lookup"><span data-stu-id="efb20-137">INPUTS</span></span>

### <span data-ttu-id="efb20-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="efb20-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>
<span data-ttu-id="efb20-139">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="efb20-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="efb20-140">System.object</span><span class="sxs-lookup"><span data-stu-id="efb20-140">System.String</span></span>

## <span data-ttu-id="efb20-141">輸出</span><span class="sxs-lookup"><span data-stu-id="efb20-141">OUTPUTS</span></span>

### <span data-ttu-id="efb20-142">System.object</span><span class="sxs-lookup"><span data-stu-id="efb20-142">System.Boolean</span></span>

## <span data-ttu-id="efb20-143">筆記</span><span class="sxs-lookup"><span data-stu-id="efb20-143">NOTES</span></span>

## <span data-ttu-id="efb20-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="efb20-144">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Stop-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
ms.openlocfilehash: a4b4ec4f24f61e188a3ab8b9cf66e8e326142bd3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965998"
---
# <span data-ttu-id="62766-101">Stop-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="62766-101">Stop-AzDataMigrationService</span></span>

## <span data-ttu-id="62766-102">摘要</span><span class="sxs-lookup"><span data-stu-id="62766-102">SYNOPSIS</span></span>
<span data-ttu-id="62766-103">停止處於執行中狀態的 Azure 資料庫移轉服務實例。</span><span class="sxs-lookup"><span data-stu-id="62766-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="62766-104">句法</span><span class="sxs-lookup"><span data-stu-id="62766-104">SYNTAX</span></span>

### <span data-ttu-id="62766-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="62766-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62766-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="62766-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62766-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62766-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62766-108">說明</span><span class="sxs-lookup"><span data-stu-id="62766-108">DESCRIPTION</span></span>
<span data-ttu-id="62766-109">Stop-AzDataMigrationService Cmdlet 會停止處於執行中狀態的 Azure 資料庫移轉服務實例。</span><span class="sxs-lookup"><span data-stu-id="62766-109">The Stop-AzDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="62766-110">示例</span><span class="sxs-lookup"><span data-stu-id="62766-110">EXAMPLES</span></span>

### <span data-ttu-id="62766-111">範例1</span><span class="sxs-lookup"><span data-stu-id="62766-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="62766-112">上述範例會根據以輸入參數傳入的服務名稱來停止名為 TestService 的 Azure Database 遷移服務實例</span><span class="sxs-lookup"><span data-stu-id="62766-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="62766-113">範例2</span><span class="sxs-lookup"><span data-stu-id="62766-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="62766-114">上述範例會根據傳遞為輸入參數的 PSDataMigrationService 物件，來停止 Azure Database 遷移服務的實例。</span><span class="sxs-lookup"><span data-stu-id="62766-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>

## <span data-ttu-id="62766-115">參數</span><span class="sxs-lookup"><span data-stu-id="62766-115">PARAMETERS</span></span>

### <span data-ttu-id="62766-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62766-116">-DefaultProfile</span></span>
<span data-ttu-id="62766-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="62766-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62766-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62766-118">-InputObject</span></span>
<span data-ttu-id="62766-119">PSDataMigrationService 物件。</span><span class="sxs-lookup"><span data-stu-id="62766-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="62766-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="62766-120">-Name</span></span>
<span data-ttu-id="62766-121">資料庫移轉服務名稱。</span><span class="sxs-lookup"><span data-stu-id="62766-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="62766-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62766-122">-PassThru</span></span>
<span data-ttu-id="62766-123">會傳回 true/false。</span><span class="sxs-lookup"><span data-stu-id="62766-123">Returns an true/false.</span></span>
<span data-ttu-id="62766-124">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="62766-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="62766-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62766-125">-ResourceGroupName</span></span>
<span data-ttu-id="62766-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="62766-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="62766-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62766-127">-ResourceId</span></span>
<span data-ttu-id="62766-128">DataMigrationService 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="62766-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="62766-129">-確認</span><span class="sxs-lookup"><span data-stu-id="62766-129">-Confirm</span></span>
<span data-ttu-id="62766-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="62766-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62766-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62766-131">-WhatIf</span></span>
<span data-ttu-id="62766-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="62766-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62766-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="62766-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62766-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62766-134">CommonParameters</span></span>
<span data-ttu-id="62766-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="62766-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62766-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="62766-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62766-137">輸入</span><span class="sxs-lookup"><span data-stu-id="62766-137">INPUTS</span></span>

### <span data-ttu-id="62766-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="62766-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="62766-139">System.object</span><span class="sxs-lookup"><span data-stu-id="62766-139">System.String</span></span>

## <span data-ttu-id="62766-140">輸出</span><span class="sxs-lookup"><span data-stu-id="62766-140">OUTPUTS</span></span>

### <span data-ttu-id="62766-141">System.object</span><span class="sxs-lookup"><span data-stu-id="62766-141">System.Boolean</span></span>

## <span data-ttu-id="62766-142">筆記</span><span class="sxs-lookup"><span data-stu-id="62766-142">NOTES</span></span>

## <span data-ttu-id="62766-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="62766-143">RELATED LINKS</span></span>

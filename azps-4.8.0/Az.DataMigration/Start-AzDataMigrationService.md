---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Start-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
ms.openlocfilehash: 2b5c24b3745007cb3a2f48432609490bd38a4186
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969279"
---
# <span data-ttu-id="60457-101">Start-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="60457-101">Start-AzDataMigrationService</span></span>

## <span data-ttu-id="60457-102">摘要</span><span class="sxs-lookup"><span data-stu-id="60457-102">SYNOPSIS</span></span>
<span data-ttu-id="60457-103">在已停止的狀態中啟動 Azure Database 遷移服務的實例。</span><span class="sxs-lookup"><span data-stu-id="60457-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="60457-104">句法</span><span class="sxs-lookup"><span data-stu-id="60457-104">SYNTAX</span></span>

### <span data-ttu-id="60457-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="60457-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60457-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60457-106">ComponentObjectParameterSet</span></span>
```
Start-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60457-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="60457-107">ResourceIdParameterSet</span></span>
```
Start-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60457-108">說明</span><span class="sxs-lookup"><span data-stu-id="60457-108">DESCRIPTION</span></span>
<span data-ttu-id="60457-109">Start-AzDataMigrationService Cmdlet 會在停止狀態中啟動 Azure Database 遷移服務的實例。</span><span class="sxs-lookup"><span data-stu-id="60457-109">The Start-AzDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="60457-110">示例</span><span class="sxs-lookup"><span data-stu-id="60457-110">EXAMPLES</span></span>

### <span data-ttu-id="60457-111">範例1</span><span class="sxs-lookup"><span data-stu-id="60457-111">Example 1</span></span>
```
PS C:\> Start-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="60457-112">上述範例會根據以輸入的服務名稱，在停止狀態中啟動名為 Test 服務的 Azure 資料庫移轉服務實例</span><span class="sxs-lookup"><span data-stu-id="60457-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="60457-113">範例2</span><span class="sxs-lookup"><span data-stu-id="60457-113">Example 2</span></span>
```
PS C:\> Start-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="60457-114">上述範例會根據以輸入參數傳入的 PSDataMigrationService 來啟動 Azure Database 遷移服務實例</span><span class="sxs-lookup"><span data-stu-id="60457-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="60457-115">參數</span><span class="sxs-lookup"><span data-stu-id="60457-115">PARAMETERS</span></span>

### <span data-ttu-id="60457-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60457-116">-DefaultProfile</span></span>
<span data-ttu-id="60457-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="60457-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60457-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60457-118">-InputObject</span></span>
<span data-ttu-id="60457-119">PSDataMigrationService 物件。</span><span class="sxs-lookup"><span data-stu-id="60457-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="60457-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="60457-120">-Name</span></span>
<span data-ttu-id="60457-121">資料庫移轉服務名稱。</span><span class="sxs-lookup"><span data-stu-id="60457-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="60457-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60457-122">-PassThru</span></span>
<span data-ttu-id="60457-123">會傳回 true/false。</span><span class="sxs-lookup"><span data-stu-id="60457-123">Returns an true/false.</span></span>
<span data-ttu-id="60457-124">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="60457-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="60457-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60457-125">-ResourceGroupName</span></span>
<span data-ttu-id="60457-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="60457-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="60457-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60457-127">-ResourceId</span></span>
<span data-ttu-id="60457-128">DataMigrationService 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="60457-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="60457-129">-確認</span><span class="sxs-lookup"><span data-stu-id="60457-129">-Confirm</span></span>
<span data-ttu-id="60457-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="60457-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60457-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60457-131">-WhatIf</span></span>
<span data-ttu-id="60457-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="60457-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60457-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="60457-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60457-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60457-134">CommonParameters</span></span>
<span data-ttu-id="60457-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="60457-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60457-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="60457-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60457-137">輸入</span><span class="sxs-lookup"><span data-stu-id="60457-137">INPUTS</span></span>

### <span data-ttu-id="60457-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="60457-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="60457-139">System.object</span><span class="sxs-lookup"><span data-stu-id="60457-139">System.String</span></span>

## <span data-ttu-id="60457-140">輸出</span><span class="sxs-lookup"><span data-stu-id="60457-140">OUTPUTS</span></span>

### <span data-ttu-id="60457-141">System.object</span><span class="sxs-lookup"><span data-stu-id="60457-141">System.Boolean</span></span>

## <span data-ttu-id="60457-142">筆記</span><span class="sxs-lookup"><span data-stu-id="60457-142">NOTES</span></span>

## <span data-ttu-id="60457-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="60457-143">RELATED LINKS</span></span>
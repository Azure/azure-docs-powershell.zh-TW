---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Start-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Start-AzDataMigrationService.md
ms.openlocfilehash: 6d0bba6429f9b836ccd1493c9074c4ccd16636da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914010"
---
# <span data-ttu-id="a1ed5-101">Start-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="a1ed5-101">Start-AzDataMigrationService</span></span>

## <span data-ttu-id="a1ed5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a1ed5-102">SYNOPSIS</span></span>
<span data-ttu-id="a1ed5-103">以停止狀態啟動 Azure 資料庫移移服務的實例。</span><span class="sxs-lookup"><span data-stu-id="a1ed5-103">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="a1ed5-104">語法</span><span class="sxs-lookup"><span data-stu-id="a1ed5-104">SYNTAX</span></span>

### <span data-ttu-id="a1ed5-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a1ed5-105">ComponentNameParameterSet (Default)</span></span>
```
Start-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1ed5-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1ed5-106">ComponentObjectParameterSet</span></span>
```
Start-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1ed5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1ed5-107">ResourceIdParameterSet</span></span>
```
Start-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1ed5-108">描述</span><span class="sxs-lookup"><span data-stu-id="a1ed5-108">DESCRIPTION</span></span>
<span data-ttu-id="a1ed5-109">此Start-AzDataMigrationService Cmdlet 會以已停止的狀態啟動 Azure 資料庫移轉服務的實例。</span><span class="sxs-lookup"><span data-stu-id="a1ed5-109">The Start-AzDataMigrationService cmdlet starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

## <span data-ttu-id="a1ed5-110">例子</span><span class="sxs-lookup"><span data-stu-id="a1ed5-110">EXAMPLES</span></span>

### <span data-ttu-id="a1ed5-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="a1ed5-111">Example 1</span></span>
```
PS C:\> Start-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="a1ed5-112">上述範例會根據以輸入方式傳遞的服務名稱，以已停止狀態啟動名為 Test Service 的 Azure 資料庫移轉服務實例</span><span class="sxs-lookup"><span data-stu-id="a1ed5-112">The above example starts an Azure Database Migration Service instance named Test Service in a stopped state based on service name passed in as input</span></span>

### <span data-ttu-id="a1ed5-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="a1ed5-113">Example 2</span></span>
```
PS C:\> Start-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="a1ed5-114">上述範例會以以輸入參數傳遞的 PSDataMigrationService 為基礎啟動 Azure 資料庫移轉服務實例</span><span class="sxs-lookup"><span data-stu-id="a1ed5-114">The above example starts an Azure Database Migration Service instance based on PSDataMigrationService passed in as input parameter</span></span>

## <span data-ttu-id="a1ed5-115">參數</span><span class="sxs-lookup"><span data-stu-id="a1ed5-115">PARAMETERS</span></span>

### <span data-ttu-id="a1ed5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1ed5-116">-DefaultProfile</span></span>
<span data-ttu-id="a1ed5-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a1ed5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1ed5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1ed5-118">-InputObject</span></span>
<span data-ttu-id="a1ed5-119">PSDataMigrationService 物件。</span><span class="sxs-lookup"><span data-stu-id="a1ed5-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="a1ed5-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="a1ed5-120">-Name</span></span>
<span data-ttu-id="a1ed5-121">資料庫移移服務名稱。</span><span class="sxs-lookup"><span data-stu-id="a1ed5-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="a1ed5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1ed5-122">-PassThru</span></span>
<span data-ttu-id="a1ed5-123">會返回 true/false。</span><span class="sxs-lookup"><span data-stu-id="a1ed5-123">Returns an true/false.</span></span>
<span data-ttu-id="a1ed5-124">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="a1ed5-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a1ed5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1ed5-125">-ResourceGroupName</span></span>
<span data-ttu-id="a1ed5-126">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1ed5-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="a1ed5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1ed5-127">-ResourceId</span></span>
<span data-ttu-id="a1ed5-128">DataMigrationService 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a1ed5-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="a1ed5-129">-確認</span><span class="sxs-lookup"><span data-stu-id="a1ed5-129">-Confirm</span></span>
<span data-ttu-id="a1ed5-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a1ed5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1ed5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1ed5-131">-WhatIf</span></span>
<span data-ttu-id="a1ed5-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a1ed5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1ed5-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a1ed5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1ed5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1ed5-134">CommonParameters</span></span>
<span data-ttu-id="a1ed5-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a1ed5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1ed5-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a1ed5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1ed5-137">輸入</span><span class="sxs-lookup"><span data-stu-id="a1ed5-137">INPUTS</span></span>

### <span data-ttu-id="a1ed5-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="a1ed5-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="a1ed5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a1ed5-139">System.String</span></span>

## <span data-ttu-id="a1ed5-140">輸出</span><span class="sxs-lookup"><span data-stu-id="a1ed5-140">OUTPUTS</span></span>

### <span data-ttu-id="a1ed5-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a1ed5-141">System.Boolean</span></span>

## <span data-ttu-id="a1ed5-142">筆記</span><span class="sxs-lookup"><span data-stu-id="a1ed5-142">NOTES</span></span>

## <span data-ttu-id="a1ed5-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1ed5-143">RELATED LINKS</span></span>

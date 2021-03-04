---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Stop-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Stop-AzDataMigrationService.md
ms.openlocfilehash: 9a6d2ba213054ea6b670205e84e3fd3893c59eea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908562"
---
# <span data-ttu-id="ad66b-101">Stop-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="ad66b-101">Stop-AzDataMigrationService</span></span>

## <span data-ttu-id="ad66b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ad66b-102">SYNOPSIS</span></span>
<span data-ttu-id="ad66b-103">停止執行中的 Azure 資料庫移移服務實例。</span><span class="sxs-lookup"><span data-stu-id="ad66b-103">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="ad66b-104">語法</span><span class="sxs-lookup"><span data-stu-id="ad66b-104">SYNTAX</span></span>

### <span data-ttu-id="ad66b-105">ComponentNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ad66b-105">ComponentNameParameterSet (Default)</span></span>
```
Stop-AzDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad66b-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad66b-106">ComponentObjectParameterSet</span></span>
```
Stop-AzDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad66b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad66b-107">ResourceIdParameterSet</span></span>
```
Stop-AzDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad66b-108">描述</span><span class="sxs-lookup"><span data-stu-id="ad66b-108">DESCRIPTION</span></span>
<span data-ttu-id="ad66b-109">此Stop-AzDataMigrationService Cmdlet 會停止執行中的 Azure 資料庫移轉服務實例。</span><span class="sxs-lookup"><span data-stu-id="ad66b-109">The Stop-AzDataMigrationService cmdlet stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

## <span data-ttu-id="ad66b-110">例子</span><span class="sxs-lookup"><span data-stu-id="ad66b-110">EXAMPLES</span></span>

### <span data-ttu-id="ad66b-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="ad66b-111">Example 1</span></span>
```
PS C:\> Stop-AzDataMigrationService -ResourceGroupName MyResourceGroup -ServiceName TestService
```

<span data-ttu-id="ad66b-112">上述範例會根據以輸入參數傳遞的服務名稱，停止名為 TestService 的 Azure 資料庫移轉服務實例</span><span class="sxs-lookup"><span data-stu-id="ad66b-112">The above example stops an instance of the Azure Database Migration Service called TestService based on service name passed in as input parameter</span></span>

### <span data-ttu-id="ad66b-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="ad66b-113">Example 2</span></span>
```
PS C:\> Stop-AzDataMigrationService -InputObject $TestService
```

<span data-ttu-id="ad66b-114">上述範例會停止以 PSDataMigrationService 物件作為輸入參數傳遞的 Azure 資料庫移轉服務實例。</span><span class="sxs-lookup"><span data-stu-id="ad66b-114">The above example stops an instance of the Azure Database Migration Service based on PSDataMigrationService object passed as input parameter.</span></span>

## <span data-ttu-id="ad66b-115">參數</span><span class="sxs-lookup"><span data-stu-id="ad66b-115">PARAMETERS</span></span>

### <span data-ttu-id="ad66b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad66b-116">-DefaultProfile</span></span>
<span data-ttu-id="ad66b-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ad66b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad66b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad66b-118">-InputObject</span></span>
<span data-ttu-id="ad66b-119">PSDataMigrationService 物件。</span><span class="sxs-lookup"><span data-stu-id="ad66b-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="ad66b-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="ad66b-120">-Name</span></span>
<span data-ttu-id="ad66b-121">資料庫移移服務名稱。</span><span class="sxs-lookup"><span data-stu-id="ad66b-121">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="ad66b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad66b-122">-PassThru</span></span>
<span data-ttu-id="ad66b-123">會返回 true/false。</span><span class="sxs-lookup"><span data-stu-id="ad66b-123">Returns an true/false.</span></span>
<span data-ttu-id="ad66b-124">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="ad66b-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ad66b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad66b-125">-ResourceGroupName</span></span>
<span data-ttu-id="ad66b-126">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad66b-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="ad66b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad66b-127">-ResourceId</span></span>
<span data-ttu-id="ad66b-128">DataMigrationService 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ad66b-128">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="ad66b-129">-確認</span><span class="sxs-lookup"><span data-stu-id="ad66b-129">-Confirm</span></span>
<span data-ttu-id="ad66b-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ad66b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad66b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad66b-131">-WhatIf</span></span>
<span data-ttu-id="ad66b-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ad66b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad66b-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad66b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad66b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad66b-134">CommonParameters</span></span>
<span data-ttu-id="ad66b-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ad66b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad66b-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ad66b-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad66b-137">輸入</span><span class="sxs-lookup"><span data-stu-id="ad66b-137">INPUTS</span></span>

### <span data-ttu-id="ad66b-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="ad66b-138">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="ad66b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ad66b-139">System.String</span></span>

## <span data-ttu-id="ad66b-140">輸出</span><span class="sxs-lookup"><span data-stu-id="ad66b-140">OUTPUTS</span></span>

### <span data-ttu-id="ad66b-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ad66b-141">System.Boolean</span></span>

## <span data-ttu-id="ad66b-142">筆記</span><span class="sxs-lookup"><span data-stu-id="ad66b-142">NOTES</span></span>

## <span data-ttu-id="ad66b-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad66b-143">RELATED LINKS</span></span>

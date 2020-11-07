---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 01213154-DD8A-412F-A23D-5D9D09BEFA3A
online version: ''
schema: 2.0.0
ms.openlocfilehash: f0602015a63d28aecb498b0830619ea1560d6066
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967687"
---
# <span data-ttu-id="b8add-101">Move-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="b8add-101">Move-AzureRouteTable</span></span>

## <span data-ttu-id="b8add-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b8add-102">SYNOPSIS</span></span>
<span data-ttu-id="b8add-103">將路由資料表遷移至 Azure 資源管理器堆疊。</span><span class="sxs-lookup"><span data-stu-id="b8add-103">Migrates a route table to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="b8add-104">句法</span><span class="sxs-lookup"><span data-stu-id="b8add-104">SYNTAX</span></span>

### <span data-ttu-id="b8add-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8add-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8add-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8add-106">AbortMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8add-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8add-107">CommitMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8add-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8add-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b8add-109">說明</span><span class="sxs-lookup"><span data-stu-id="b8add-109">DESCRIPTION</span></span>
<span data-ttu-id="b8add-110">**AzureRouteTable** Cmdlet 會將路由資料表遷移至 Azure 資源管理器堆疊中的資源群組。</span><span class="sxs-lookup"><span data-stu-id="b8add-110">The **Move-AzureRouteTable** cmdlet migrates a route table to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="b8add-111">示例</span><span class="sxs-lookup"><span data-stu-id="b8add-111">EXAMPLES</span></span>

### <span data-ttu-id="b8add-112">sr-1</span><span class="sxs-lookup"><span data-stu-id="b8add-112">1:</span></span>
```

```

## <span data-ttu-id="b8add-113">參數</span><span class="sxs-lookup"><span data-stu-id="b8add-113">PARAMETERS</span></span>

### <span data-ttu-id="b8add-114">-中止</span><span class="sxs-lookup"><span data-stu-id="b8add-114">-Abort</span></span>
<span data-ttu-id="b8add-115">表示此 Cmdlet 會取消路由表遷移。</span><span class="sxs-lookup"><span data-stu-id="b8add-115">Indicates that this cmdlet cancels the route table migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AbortMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8add-116">-認可</span><span class="sxs-lookup"><span data-stu-id="b8add-116">-Commit</span></span>
<span data-ttu-id="b8add-117">表示此 Cmdlet 會啟動路由表遷移。</span><span class="sxs-lookup"><span data-stu-id="b8add-117">Indicates that this cmdlet starts the route table migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CommitMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8add-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b8add-118">-InformationAction</span></span>
<span data-ttu-id="b8add-119">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="b8add-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b8add-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b8add-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b8add-121">持續</span><span class="sxs-lookup"><span data-stu-id="b8add-121">Continue</span></span>
- <span data-ttu-id="b8add-122">理會</span><span class="sxs-lookup"><span data-stu-id="b8add-122">Ignore</span></span>
- <span data-ttu-id="b8add-123">看</span><span class="sxs-lookup"><span data-stu-id="b8add-123">Inquire</span></span>
- <span data-ttu-id="b8add-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b8add-124">SilentlyContinue</span></span>
- <span data-ttu-id="b8add-125">停止</span><span class="sxs-lookup"><span data-stu-id="b8add-125">Stop</span></span>
- <span data-ttu-id="b8add-126">封存</span><span class="sxs-lookup"><span data-stu-id="b8add-126">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8add-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b8add-127">-InformationVariable</span></span>
<span data-ttu-id="b8add-128">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="b8add-128">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8add-129">-準備</span><span class="sxs-lookup"><span data-stu-id="b8add-129">-Prepare</span></span>
<span data-ttu-id="b8add-130">表示此 Cmdlet 準備要遷移的路由表。</span><span class="sxs-lookup"><span data-stu-id="b8add-130">Indicates that this cmdlet prepares the route table for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8add-131">-設定檔</span><span class="sxs-lookup"><span data-stu-id="b8add-131">-Profile</span></span>
<span data-ttu-id="b8add-132">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b8add-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b8add-133">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="b8add-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8add-134">-RouteTableName</span><span class="sxs-lookup"><span data-stu-id="b8add-134">-RouteTableName</span></span>
<span data-ttu-id="b8add-135">指定此 Cmdlet 遷移之路由資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8add-135">Specifies the name of the route table that this cmdlet migrates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8add-136">-驗證</span><span class="sxs-lookup"><span data-stu-id="b8add-136">-Validate</span></span>
<span data-ttu-id="b8add-137">指定此 Cmdlet 會驗證路由資料表的遷移。</span><span class="sxs-lookup"><span data-stu-id="b8add-137">Specifies that this cmdlet validates the route table for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ValidateMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8add-138">-確認</span><span class="sxs-lookup"><span data-stu-id="b8add-138">-Confirm</span></span>
<span data-ttu-id="b8add-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b8add-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8add-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8add-140">-WhatIf</span></span>
<span data-ttu-id="b8add-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b8add-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8add-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b8add-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8add-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8add-143">CommonParameters</span></span>
<span data-ttu-id="b8add-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b8add-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8add-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b8add-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8add-146">輸入</span><span class="sxs-lookup"><span data-stu-id="b8add-146">INPUTS</span></span>

## <span data-ttu-id="b8add-147">輸出</span><span class="sxs-lookup"><span data-stu-id="b8add-147">OUTPUTS</span></span>

## <span data-ttu-id="b8add-148">筆記</span><span class="sxs-lookup"><span data-stu-id="b8add-148">NOTES</span></span>

## <span data-ttu-id="b8add-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8add-149">RELATED LINKS</span></span>

[<span data-ttu-id="b8add-150">移動流覽 AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b8add-150">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="b8add-151">移動流覽 AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="b8add-151">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="b8add-152">移動流覽 AzureService</span><span class="sxs-lookup"><span data-stu-id="b8add-152">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="b8add-153">移動流覽 AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b8add-153">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="b8add-154">移動流覽 AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b8add-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)



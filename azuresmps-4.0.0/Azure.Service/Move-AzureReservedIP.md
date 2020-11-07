---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D1A4FA07-C25E-472B-9C64-695AD41274FA
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb8b6a502d6abe5520cadcf776ece1f077c7d91f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967688"
---
# <span data-ttu-id="1f12e-101">Move-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="1f12e-101">Move-AzureReservedIP</span></span>

## <span data-ttu-id="1f12e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1f12e-102">SYNOPSIS</span></span>
<span data-ttu-id="1f12e-103">將保留的 IP 位址遷移至 Azure 資源管理器堆疊。</span><span class="sxs-lookup"><span data-stu-id="1f12e-103">Migrates a reserved IP address to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="1f12e-104">句法</span><span class="sxs-lookup"><span data-stu-id="1f12e-104">SYNTAX</span></span>

### <span data-ttu-id="1f12e-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f12e-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f12e-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f12e-106">AbortMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f12e-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f12e-107">CommitMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f12e-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f12e-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f12e-109">說明</span><span class="sxs-lookup"><span data-stu-id="1f12e-109">DESCRIPTION</span></span>
<span data-ttu-id="1f12e-110">**AzureReservedIP** Cmdlet 會將保留 IP 位址遷移至 Azure 資源管理器堆疊中的資源群組。</span><span class="sxs-lookup"><span data-stu-id="1f12e-110">The **Move-AzureReservedIP** cmdlet migrates a reserved IP address to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="1f12e-111">示例</span><span class="sxs-lookup"><span data-stu-id="1f12e-111">EXAMPLES</span></span>

### <span data-ttu-id="1f12e-112">sr-1</span><span class="sxs-lookup"><span data-stu-id="1f12e-112">1:</span></span>
```

```

## <span data-ttu-id="1f12e-113">參數</span><span class="sxs-lookup"><span data-stu-id="1f12e-113">PARAMETERS</span></span>

### <span data-ttu-id="1f12e-114">-中止</span><span class="sxs-lookup"><span data-stu-id="1f12e-114">-Abort</span></span>
<span data-ttu-id="1f12e-115">表示此 Cmdlet 會取消保留的 IP 位址遷移。</span><span class="sxs-lookup"><span data-stu-id="1f12e-115">Indicates that this cmdlet cancels the reserved IP address migration.</span></span>

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

### <span data-ttu-id="1f12e-116">-認可</span><span class="sxs-lookup"><span data-stu-id="1f12e-116">-Commit</span></span>
<span data-ttu-id="1f12e-117">表示此 Cmdlet 會啟動保留的 IP 位址遷移。</span><span class="sxs-lookup"><span data-stu-id="1f12e-117">Indicates that this cmdlet starts the reserved IP address migration.</span></span>

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

### <span data-ttu-id="1f12e-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1f12e-118">-InformationAction</span></span>
<span data-ttu-id="1f12e-119">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="1f12e-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1f12e-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1f12e-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1f12e-121">持續</span><span class="sxs-lookup"><span data-stu-id="1f12e-121">Continue</span></span>
- <span data-ttu-id="1f12e-122">理會</span><span class="sxs-lookup"><span data-stu-id="1f12e-122">Ignore</span></span>
- <span data-ttu-id="1f12e-123">看</span><span class="sxs-lookup"><span data-stu-id="1f12e-123">Inquire</span></span>
- <span data-ttu-id="1f12e-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1f12e-124">SilentlyContinue</span></span>
- <span data-ttu-id="1f12e-125">停止</span><span class="sxs-lookup"><span data-stu-id="1f12e-125">Stop</span></span>
- <span data-ttu-id="1f12e-126">封存</span><span class="sxs-lookup"><span data-stu-id="1f12e-126">Suspend</span></span>

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

### <span data-ttu-id="1f12e-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1f12e-127">-InformationVariable</span></span>
<span data-ttu-id="1f12e-128">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="1f12e-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1f12e-129">-準備</span><span class="sxs-lookup"><span data-stu-id="1f12e-129">-Prepare</span></span>
<span data-ttu-id="1f12e-130">表示此 Cmdlet 準備好用來進行遷移的保留 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="1f12e-130">Indicates that this cmdlet prepares the reserved IP address for migration.</span></span>

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

### <span data-ttu-id="1f12e-131">-設定檔</span><span class="sxs-lookup"><span data-stu-id="1f12e-131">-Profile</span></span>
<span data-ttu-id="1f12e-132">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="1f12e-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1f12e-133">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="1f12e-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1f12e-134">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="1f12e-134">-ReservedIPName</span></span>
<span data-ttu-id="1f12e-135">指定此 Cmdlet 遷移之保留 IP 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="1f12e-135">Specifies the name of the reserved IP address that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="1f12e-136">-驗證</span><span class="sxs-lookup"><span data-stu-id="1f12e-136">-Validate</span></span>
<span data-ttu-id="1f12e-137">指定此 Cmdlet 會驗證用於遷移的保留 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="1f12e-137">Specifies that this cmdlet validates the reserved IP address for migration.</span></span>

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

### <span data-ttu-id="1f12e-138">-確認</span><span class="sxs-lookup"><span data-stu-id="1f12e-138">-Confirm</span></span>
<span data-ttu-id="1f12e-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1f12e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f12e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f12e-140">-WhatIf</span></span>
<span data-ttu-id="1f12e-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1f12e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f12e-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1f12e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f12e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f12e-143">CommonParameters</span></span>
<span data-ttu-id="1f12e-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1f12e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f12e-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1f12e-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f12e-146">輸入</span><span class="sxs-lookup"><span data-stu-id="1f12e-146">INPUTS</span></span>

## <span data-ttu-id="1f12e-147">輸出</span><span class="sxs-lookup"><span data-stu-id="1f12e-147">OUTPUTS</span></span>

## <span data-ttu-id="1f12e-148">筆記</span><span class="sxs-lookup"><span data-stu-id="1f12e-148">NOTES</span></span>

## <span data-ttu-id="1f12e-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f12e-149">RELATED LINKS</span></span>

[<span data-ttu-id="1f12e-150">移動流覽 AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1f12e-150">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="1f12e-151">移動流覽 AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="1f12e-151">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="1f12e-152">移動流覽 AzureService</span><span class="sxs-lookup"><span data-stu-id="1f12e-152">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="1f12e-153">移動流覽 AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1f12e-153">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="1f12e-154">移動流覽 AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1f12e-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)



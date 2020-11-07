---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 27ECCBAD-0CFE-4309-B590-BB60E1872ED5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d96f02374eb266cb9eaa3c1cc7c200a4f154043
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967689"
---
# <span data-ttu-id="af990-101">Move-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="af990-101">Move-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="af990-102">摘要</span><span class="sxs-lookup"><span data-stu-id="af990-102">SYNOPSIS</span></span>
<span data-ttu-id="af990-103">將網路安全群組遷移至 Azure 資源管理器堆疊。</span><span class="sxs-lookup"><span data-stu-id="af990-103">Migrates a Network Security Group to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="af990-104">句法</span><span class="sxs-lookup"><span data-stu-id="af990-104">SYNTAX</span></span>

### <span data-ttu-id="af990-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="af990-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af990-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="af990-106">AbortMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af990-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="af990-107">CommitMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="af990-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="af990-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af990-109">說明</span><span class="sxs-lookup"><span data-stu-id="af990-109">DESCRIPTION</span></span>
<span data-ttu-id="af990-110">**AzureNetworkSecurityGroup** Cmdlet 會將網路安全性群組遷移至 Azure 資源管理器堆疊中的資源群組。</span><span class="sxs-lookup"><span data-stu-id="af990-110">The **Move-AzureNetworkSecurityGroup** cmdlet migrates a Network Security Group to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="af990-111">示例</span><span class="sxs-lookup"><span data-stu-id="af990-111">EXAMPLES</span></span>

### <span data-ttu-id="af990-112">sr-1</span><span class="sxs-lookup"><span data-stu-id="af990-112">1:</span></span>
```

```

## <span data-ttu-id="af990-113">參數</span><span class="sxs-lookup"><span data-stu-id="af990-113">PARAMETERS</span></span>

### <span data-ttu-id="af990-114">-中止</span><span class="sxs-lookup"><span data-stu-id="af990-114">-Abort</span></span>
<span data-ttu-id="af990-115">表示此 Cmdlet 會取消網路安全群組遷移。</span><span class="sxs-lookup"><span data-stu-id="af990-115">Indicates that this cmdlet cancels the Network Security Group migration.</span></span>

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

### <span data-ttu-id="af990-116">-認可</span><span class="sxs-lookup"><span data-stu-id="af990-116">-Commit</span></span>
<span data-ttu-id="af990-117">表示此 Cmdlet 會啟動網路安全群組遷移。</span><span class="sxs-lookup"><span data-stu-id="af990-117">Indicates that this cmdlet starts the Network Security Group migration.</span></span>

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

### <span data-ttu-id="af990-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="af990-118">-InformationAction</span></span>
<span data-ttu-id="af990-119">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="af990-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="af990-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="af990-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="af990-121">持續</span><span class="sxs-lookup"><span data-stu-id="af990-121">Continue</span></span>
- <span data-ttu-id="af990-122">理會</span><span class="sxs-lookup"><span data-stu-id="af990-122">Ignore</span></span>
- <span data-ttu-id="af990-123">看</span><span class="sxs-lookup"><span data-stu-id="af990-123">Inquire</span></span>
- <span data-ttu-id="af990-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="af990-124">SilentlyContinue</span></span>
- <span data-ttu-id="af990-125">停止</span><span class="sxs-lookup"><span data-stu-id="af990-125">Stop</span></span>
- <span data-ttu-id="af990-126">封存</span><span class="sxs-lookup"><span data-stu-id="af990-126">Suspend</span></span>

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

### <span data-ttu-id="af990-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="af990-127">-InformationVariable</span></span>
<span data-ttu-id="af990-128">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="af990-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="af990-129">-NetworkSecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="af990-129">-NetworkSecurityGroupName</span></span>
<span data-ttu-id="af990-130">指定此 Cmdlet 遷移之網路安全性群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="af990-130">Specifies the name of the Network Security Group that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="af990-131">-準備</span><span class="sxs-lookup"><span data-stu-id="af990-131">-Prepare</span></span>
<span data-ttu-id="af990-132">表示此 Cmdlet 為遷移的網路安全群組做好準備。</span><span class="sxs-lookup"><span data-stu-id="af990-132">Indicates that this cmdlet prepares the Network Security Group for migration.</span></span>

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

### <span data-ttu-id="af990-133">-設定檔</span><span class="sxs-lookup"><span data-stu-id="af990-133">-Profile</span></span>
<span data-ttu-id="af990-134">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="af990-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="af990-135">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="af990-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="af990-136">-驗證</span><span class="sxs-lookup"><span data-stu-id="af990-136">-Validate</span></span>
<span data-ttu-id="af990-137">指定此 Cmdlet 會驗證用於遷移的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="af990-137">Specifies that this cmdlet validates the Network Security Group for migration.</span></span>

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

### <span data-ttu-id="af990-138">-確認</span><span class="sxs-lookup"><span data-stu-id="af990-138">-Confirm</span></span>
<span data-ttu-id="af990-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="af990-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af990-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af990-140">-WhatIf</span></span>
<span data-ttu-id="af990-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="af990-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af990-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="af990-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af990-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af990-143">CommonParameters</span></span>
<span data-ttu-id="af990-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="af990-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af990-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="af990-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af990-146">輸入</span><span class="sxs-lookup"><span data-stu-id="af990-146">INPUTS</span></span>

## <span data-ttu-id="af990-147">輸出</span><span class="sxs-lookup"><span data-stu-id="af990-147">OUTPUTS</span></span>

## <span data-ttu-id="af990-148">筆記</span><span class="sxs-lookup"><span data-stu-id="af990-148">NOTES</span></span>

## <span data-ttu-id="af990-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="af990-149">RELATED LINKS</span></span>

[<span data-ttu-id="af990-150">移動流覽 AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="af990-150">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="af990-151">移動流覽 AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="af990-151">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="af990-152">移動流覽 AzureService</span><span class="sxs-lookup"><span data-stu-id="af990-152">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="af990-153">移動流覽 AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="af990-153">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="af990-154">移動流覽 AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="af990-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)



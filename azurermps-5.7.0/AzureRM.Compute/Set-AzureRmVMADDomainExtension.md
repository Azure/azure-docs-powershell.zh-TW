---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
ms.openlocfilehash: b0af0f205f26862c20dd50e6181d2c11cd050dd1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444696"
---
# <span data-ttu-id="e1d85-101">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="e1d85-101">Set-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="e1d85-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e1d85-102">SYNOPSIS</span></span>
<span data-ttu-id="e1d85-103">新增 AD 網域延伸至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="e1d85-103">Adds an AD domain extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1d85-104">句法</span><span class="sxs-lookup"><span data-stu-id="e1d85-104">SYNTAX</span></span>

```
Set-AzureRmVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1d85-105">說明</span><span class="sxs-lookup"><span data-stu-id="e1d85-105">DESCRIPTION</span></span>
<span data-ttu-id="e1d85-106">**AzureRmVMADDomainExtension** Cmdlet 會將 Azure Active DIRECTORY (AD) 網域虛擬電腦延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="e1d85-106">The **Set-AzureRmVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="e1d85-107">此延伸功能可讓您的虛擬機器加入網域。</span><span class="sxs-lookup"><span data-stu-id="e1d85-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="e1d85-108">示例</span><span class="sxs-lookup"><span data-stu-id="e1d85-108">EXAMPLES</span></span>

## <span data-ttu-id="e1d85-109">參數</span><span class="sxs-lookup"><span data-stu-id="e1d85-109">PARAMETERS</span></span>

### <span data-ttu-id="e1d85-110">-認證</span><span class="sxs-lookup"><span data-stu-id="e1d85-110">-Credential</span></span>
<span data-ttu-id="e1d85-111">指定虛擬機器的使用者名稱和密碼作為 **PSCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="e1d85-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="e1d85-112">若要取得認證，請使用 Get-Credential Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e1d85-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="e1d85-113">如需詳細資訊，請輸入 `Get-Help Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="e1d85-113">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d85-114">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="e1d85-114">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="e1d85-115">表示此 Cmdlet 會停用延伸次要版本的自動升級。</span><span class="sxs-lookup"><span data-stu-id="e1d85-115">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d85-116">-功能變數名稱</span><span class="sxs-lookup"><span data-stu-id="e1d85-116">-DomainName</span></span>
<span data-ttu-id="e1d85-117">指定網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1d85-117">Specifies the name of the domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d85-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="e1d85-118">-ForceRerun</span></span>
<span data-ttu-id="e1d85-119">表示此 Cmdlet 會強制在虛擬機器上重新執行相同的延伸設定，而不需卸載並重新安裝延伸。</span><span class="sxs-lookup"><span data-stu-id="e1d85-119">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="e1d85-120">這個值可以是與目前值不同的任何字串。</span><span class="sxs-lookup"><span data-stu-id="e1d85-120">The value can be any string different from the current value.</span></span>

<span data-ttu-id="e1d85-121">如果 forceUpdateTag 未變更，處理常式仍會套用公用或受保護設定的更新。</span><span class="sxs-lookup"><span data-stu-id="e1d85-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d85-122">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="e1d85-122">-JoinOption</span></span>
<span data-ttu-id="e1d85-123">指定 [連接] 選項。</span><span class="sxs-lookup"><span data-stu-id="e1d85-123">Specifies the join option.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d85-124">-位置</span><span class="sxs-lookup"><span data-stu-id="e1d85-124">-Location</span></span>
<span data-ttu-id="e1d85-125">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="e1d85-125">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d85-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="e1d85-126">-Name</span></span>
<span data-ttu-id="e1d85-127">指定要新增之網域延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1d85-127">Specifies the name of the domain extension to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d85-128">-OUPath</span><span class="sxs-lookup"><span data-stu-id="e1d85-128">-OUPath</span></span>
<span data-ttu-id="e1d85-129">指定網域帳戶 (OU) 的組織單位。</span><span class="sxs-lookup"><span data-stu-id="e1d85-129">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="e1d85-130">在引號中輸入 OU 的完整辨識名稱。</span><span class="sxs-lookup"><span data-stu-id="e1d85-130">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="e1d85-131">預設值是網域中電腦物件的預設 OU。</span><span class="sxs-lookup"><span data-stu-id="e1d85-131">The default value is the default OU for machine objects in the domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d85-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1d85-132">-ResourceGroupName</span></span>
<span data-ttu-id="e1d85-133">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1d85-133">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d85-134">-重新開機</span><span class="sxs-lookup"><span data-stu-id="e1d85-134">-Restart</span></span>
<span data-ttu-id="e1d85-135">表示此 Cmdlet 會重新開機虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="e1d85-135">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="e1d85-136">通常需要重新開機，才能使變更生效。</span><span class="sxs-lookup"><span data-stu-id="e1d85-136">A restart is often required to make the change effective.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d85-137">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="e1d85-137">-TypeHandlerVersion</span></span>
<span data-ttu-id="e1d85-138">指定網域延伸的版本。</span><span class="sxs-lookup"><span data-stu-id="e1d85-138">Specifies the version of the domain extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d85-139">-VMName</span><span class="sxs-lookup"><span data-stu-id="e1d85-139">-VMName</span></span>
<span data-ttu-id="e1d85-140">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1d85-140">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1d85-141">-確認</span><span class="sxs-lookup"><span data-stu-id="e1d85-141">-Confirm</span></span>
<span data-ttu-id="e1d85-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e1d85-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1d85-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1d85-143">-WhatIf</span></span>
<span data-ttu-id="e1d85-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e1d85-144">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="e1d85-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e1d85-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1d85-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1d85-146">CommonParameters</span></span>
<span data-ttu-id="e1d85-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e1d85-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1d85-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e1d85-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1d85-149">輸入</span><span class="sxs-lookup"><span data-stu-id="e1d85-149">INPUTS</span></span>

### <span data-ttu-id="e1d85-150">所有</span><span class="sxs-lookup"><span data-stu-id="e1d85-150">None</span></span>
<span data-ttu-id="e1d85-151">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="e1d85-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e1d85-152">輸出</span><span class="sxs-lookup"><span data-stu-id="e1d85-152">OUTPUTS</span></span>

## <span data-ttu-id="e1d85-153">筆記</span><span class="sxs-lookup"><span data-stu-id="e1d85-153">NOTES</span></span>

## <span data-ttu-id="e1d85-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1d85-154">RELATED LINKS</span></span>

[<span data-ttu-id="e1d85-155">AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="e1d85-155">Get-AzureRmVMADDomainExtension</span></span>](./Get-AzureRmVMADDomainExtension.md)

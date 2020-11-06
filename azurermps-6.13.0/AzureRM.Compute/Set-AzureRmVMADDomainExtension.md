---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMADDomainExtension.md
ms.openlocfilehash: e0d36e8ddc239d1d075b79e0c91df645d671c6a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456112"
---
# <span data-ttu-id="6befa-101">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="6befa-101">Set-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="6befa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6befa-102">SYNOPSIS</span></span>
<span data-ttu-id="6befa-103">新增 AD 網域延伸至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6befa-103">Adds an AD domain extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6befa-104">句法</span><span class="sxs-lookup"><span data-stu-id="6befa-104">SYNTAX</span></span>

```
Set-AzureRmVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6befa-105">說明</span><span class="sxs-lookup"><span data-stu-id="6befa-105">DESCRIPTION</span></span>
<span data-ttu-id="6befa-106">**AzureRmVMADDomainExtension** Cmdlet 會將 Azure Active DIRECTORY (AD) 網域虛擬電腦延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6befa-106">The **Set-AzureRmVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="6befa-107">此延伸功能可讓您的虛擬機器加入網域。</span><span class="sxs-lookup"><span data-stu-id="6befa-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="6befa-108">示例</span><span class="sxs-lookup"><span data-stu-id="6befa-108">EXAMPLES</span></span>

## <span data-ttu-id="6befa-109">參數</span><span class="sxs-lookup"><span data-stu-id="6befa-109">PARAMETERS</span></span>

### <span data-ttu-id="6befa-110">-認證</span><span class="sxs-lookup"><span data-stu-id="6befa-110">-Credential</span></span>
<span data-ttu-id="6befa-111">指定虛擬機器的使用者名稱和密碼作為 **PSCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="6befa-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="6befa-112">若要取得認證，請使用 Get-Credential Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6befa-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="6befa-113">如需詳細資訊，請輸入 `Get-Help Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="6befa-113">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6befa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6befa-114">-DefaultProfile</span></span>
<span data-ttu-id="6befa-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6befa-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6befa-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="6befa-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="6befa-117">表示此 Cmdlet 會停用延伸次要版本的自動升級。</span><span class="sxs-lookup"><span data-stu-id="6befa-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6befa-118">-功能變數名稱</span><span class="sxs-lookup"><span data-stu-id="6befa-118">-DomainName</span></span>
<span data-ttu-id="6befa-119">指定網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="6befa-119">Specifies the name of the domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6befa-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="6befa-120">-ForceRerun</span></span>
<span data-ttu-id="6befa-121">表示此 Cmdlet 會強制在虛擬機器上重新執行相同的延伸設定，而不需卸載並重新安裝延伸。</span><span class="sxs-lookup"><span data-stu-id="6befa-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="6befa-122">這個值可以是與目前值不同的任何字串。</span><span class="sxs-lookup"><span data-stu-id="6befa-122">The value can be any string different from the current value.</span></span>
<span data-ttu-id="6befa-123">如果 forceUpdateTag 未變更，處理常式仍會套用公用或受保護設定的更新。</span><span class="sxs-lookup"><span data-stu-id="6befa-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6befa-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="6befa-124">-JoinOption</span></span>
<span data-ttu-id="6befa-125">指定 [連接] 選項。</span><span class="sxs-lookup"><span data-stu-id="6befa-125">Specifies the join option.</span></span> <span data-ttu-id="6befa-126">如需連接選項，請參閱 [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span><span class="sxs-lookup"><span data-stu-id="6befa-126">For join options see [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6befa-127">-位置</span><span class="sxs-lookup"><span data-stu-id="6befa-127">-Location</span></span>
<span data-ttu-id="6befa-128">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="6befa-128">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6befa-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="6befa-129">-Name</span></span>
<span data-ttu-id="6befa-130">指定要新增之網域延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="6befa-130">Specifies the name of the domain extension to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6befa-131">-OUPath</span><span class="sxs-lookup"><span data-stu-id="6befa-131">-OUPath</span></span>
<span data-ttu-id="6befa-132">指定網域帳戶 (OU) 的組織單位。</span><span class="sxs-lookup"><span data-stu-id="6befa-132">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="6befa-133">在引號中輸入 OU 的完整辨識名稱。</span><span class="sxs-lookup"><span data-stu-id="6befa-133">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="6befa-134">預設值是網域中電腦物件的預設 OU。</span><span class="sxs-lookup"><span data-stu-id="6befa-134">The default value is the default OU for machine objects in the domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6befa-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6befa-135">-ResourceGroupName</span></span>
<span data-ttu-id="6befa-136">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6befa-136">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6befa-137">-重新開機</span><span class="sxs-lookup"><span data-stu-id="6befa-137">-Restart</span></span>
<span data-ttu-id="6befa-138">表示此 Cmdlet 會重新開機虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6befa-138">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="6befa-139">通常需要重新開機，才能使變更生效。</span><span class="sxs-lookup"><span data-stu-id="6befa-139">A restart is often required to make the change effective.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6befa-140">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="6befa-140">-TypeHandlerVersion</span></span>
<span data-ttu-id="6befa-141">指定網域延伸的版本。</span><span class="sxs-lookup"><span data-stu-id="6befa-141">Specifies the version of the domain extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6befa-142">-VMName</span><span class="sxs-lookup"><span data-stu-id="6befa-142">-VMName</span></span>
<span data-ttu-id="6befa-143">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="6befa-143">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6befa-144">-確認</span><span class="sxs-lookup"><span data-stu-id="6befa-144">-Confirm</span></span>
<span data-ttu-id="6befa-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6befa-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6befa-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6befa-146">-WhatIf</span></span>
<span data-ttu-id="6befa-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6befa-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6befa-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6befa-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6befa-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6befa-149">CommonParameters</span></span>
<span data-ttu-id="6befa-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6befa-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6befa-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6befa-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6befa-152">輸入</span><span class="sxs-lookup"><span data-stu-id="6befa-152">INPUTS</span></span>

### <span data-ttu-id="6befa-153">System.object</span><span class="sxs-lookup"><span data-stu-id="6befa-153">System.String</span></span>

### <span data-ttu-id="6befa-154">System.object "1 [[System. UInt32，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="6befa-154">System.Nullable\`1[[System.UInt32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="6befa-155">系統管理. PSCredential</span><span class="sxs-lookup"><span data-stu-id="6befa-155">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="6befa-156">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="6befa-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6befa-157">輸出</span><span class="sxs-lookup"><span data-stu-id="6befa-157">OUTPUTS</span></span>

### <span data-ttu-id="6befa-158">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="6befa-158">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="6befa-159">筆記</span><span class="sxs-lookup"><span data-stu-id="6befa-159">NOTES</span></span>

## <span data-ttu-id="6befa-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="6befa-160">RELATED LINKS</span></span>

[<span data-ttu-id="6befa-161">AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="6befa-161">Get-AzureRmVMADDomainExtension</span></span>](./Get-AzureRmVMADDomainExtension.md)

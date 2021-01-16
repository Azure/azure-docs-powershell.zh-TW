---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
ms.openlocfilehash: 1ea90503c1d022aa5a1925fa489e2ee63f4560ee
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280892"
---
# <span data-ttu-id="2766c-101">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="2766c-101">Set-AzVMADDomainExtension</span></span>

## <span data-ttu-id="2766c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2766c-102">SYNOPSIS</span></span>
<span data-ttu-id="2766c-103">新增 AD 網域延伸至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2766c-103">Adds an AD domain extension to a virtual machine.</span></span>

## <span data-ttu-id="2766c-104">句法</span><span class="sxs-lookup"><span data-stu-id="2766c-104">SYNTAX</span></span>

```
Set-AzVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2766c-105">說明</span><span class="sxs-lookup"><span data-stu-id="2766c-105">DESCRIPTION</span></span>
<span data-ttu-id="2766c-106">**AzVMADDomainExtension** Cmdlet 會將 Azure Active DIRECTORY (AD) 網域虛擬電腦延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2766c-106">The **Set-AzVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="2766c-107">此延伸功能可讓您的虛擬機器加入網域。</span><span class="sxs-lookup"><span data-stu-id="2766c-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="2766c-108">示例</span><span class="sxs-lookup"><span data-stu-id="2766c-108">EXAMPLES</span></span>

## <span data-ttu-id="2766c-109">參數</span><span class="sxs-lookup"><span data-stu-id="2766c-109">PARAMETERS</span></span>

### <span data-ttu-id="2766c-110">-認證</span><span class="sxs-lookup"><span data-stu-id="2766c-110">-Credential</span></span>
<span data-ttu-id="2766c-111">指定虛擬機器的使用者名稱和密碼作為 **PSCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="2766c-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="2766c-112">若要取得認證，請使用 Get-Credential Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2766c-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="2766c-113">如需詳細資訊，請輸入 `Get-Help Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="2766c-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="2766c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2766c-114">-DefaultProfile</span></span>
<span data-ttu-id="2766c-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2766c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2766c-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="2766c-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="2766c-117">表示此 Cmdlet 會停用延伸次要版本的自動升級。</span><span class="sxs-lookup"><span data-stu-id="2766c-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="2766c-118">-功能變數名稱</span><span class="sxs-lookup"><span data-stu-id="2766c-118">-DomainName</span></span>
<span data-ttu-id="2766c-119">指定網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="2766c-119">Specifies the name of the domain.</span></span>

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

### <span data-ttu-id="2766c-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="2766c-120">-ForceRerun</span></span>
<span data-ttu-id="2766c-121">表示此 Cmdlet 會強制在虛擬機器上重新執行相同的延伸設定，而不需卸載並重新安裝延伸。</span><span class="sxs-lookup"><span data-stu-id="2766c-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="2766c-122">這個值可以是與目前值不同的任何字串。</span><span class="sxs-lookup"><span data-stu-id="2766c-122">The value can be any string different from the current value.</span></span>
<span data-ttu-id="2766c-123">如果 forceUpdateTag 未變更，處理常式仍會套用公用或受保護設定的更新。</span><span class="sxs-lookup"><span data-stu-id="2766c-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="2766c-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="2766c-124">-JoinOption</span></span>
<span data-ttu-id="2766c-125">指定 [連接] 選項。</span><span class="sxs-lookup"><span data-stu-id="2766c-125">Specifies the join option.</span></span> <span data-ttu-id="2766c-126">如需連接選項，請參閱 [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span><span class="sxs-lookup"><span data-stu-id="2766c-126">For join options see [fJoinOptions](https://docs.microsoft.com/en-us/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span></span>

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

### <span data-ttu-id="2766c-127">-位置</span><span class="sxs-lookup"><span data-stu-id="2766c-127">-Location</span></span>
<span data-ttu-id="2766c-128">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="2766c-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="2766c-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="2766c-129">-Name</span></span>
<span data-ttu-id="2766c-130">指定要新增之網域延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="2766c-130">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="2766c-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2766c-131">-NoWait</span></span>
<span data-ttu-id="2766c-132">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="2766c-132">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="2766c-133">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="2766c-133">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="2766c-134">-OUPath</span><span class="sxs-lookup"><span data-stu-id="2766c-134">-OUPath</span></span>
<span data-ttu-id="2766c-135">指定網域帳戶 (OU) 的組織單位。</span><span class="sxs-lookup"><span data-stu-id="2766c-135">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="2766c-136">在引號中輸入 OU 的完整辨識名稱。</span><span class="sxs-lookup"><span data-stu-id="2766c-136">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="2766c-137">預設值是網域中電腦物件的預設 OU。</span><span class="sxs-lookup"><span data-stu-id="2766c-137">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="2766c-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2766c-138">-ResourceGroupName</span></span>
<span data-ttu-id="2766c-139">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2766c-139">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2766c-140">-重新開機</span><span class="sxs-lookup"><span data-stu-id="2766c-140">-Restart</span></span>
<span data-ttu-id="2766c-141">表示此 Cmdlet 會重新開機虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2766c-141">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="2766c-142">通常需要重新開機，才能使變更生效。</span><span class="sxs-lookup"><span data-stu-id="2766c-142">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="2766c-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="2766c-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="2766c-144">指定網域延伸的版本。</span><span class="sxs-lookup"><span data-stu-id="2766c-144">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="2766c-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="2766c-145">-VMName</span></span>
<span data-ttu-id="2766c-146">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="2766c-146">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="2766c-147">-確認</span><span class="sxs-lookup"><span data-stu-id="2766c-147">-Confirm</span></span>
<span data-ttu-id="2766c-148">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2766c-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2766c-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2766c-149">-WhatIf</span></span>
<span data-ttu-id="2766c-150">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2766c-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2766c-151">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2766c-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2766c-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2766c-152">CommonParameters</span></span>
<span data-ttu-id="2766c-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2766c-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2766c-154">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2766c-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2766c-155">輸入</span><span class="sxs-lookup"><span data-stu-id="2766c-155">INPUTS</span></span>

### <span data-ttu-id="2766c-156">System.object</span><span class="sxs-lookup"><span data-stu-id="2766c-156">System.String</span></span>

### <span data-ttu-id="2766c-157">系統. Nullable "1 [[System. UInt32，System.object CoreLib，Version = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2766c-157">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2766c-158">系統管理. PSCredential</span><span class="sxs-lookup"><span data-stu-id="2766c-158">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="2766c-159">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="2766c-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2766c-160">輸出</span><span class="sxs-lookup"><span data-stu-id="2766c-160">OUTPUTS</span></span>

### <span data-ttu-id="2766c-161">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="2766c-161">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2766c-162">筆記</span><span class="sxs-lookup"><span data-stu-id="2766c-162">NOTES</span></span>

## <span data-ttu-id="2766c-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="2766c-163">RELATED LINKS</span></span>

[<span data-ttu-id="2766c-164">AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="2766c-164">Get-AzVMADDomainExtension</span></span>](./Get-AzVMADDomainExtension.md)

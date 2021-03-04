---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 65BF37D3-4FCE-48A3-BC5D-01AA20FEB6CA
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMADDomainExtension.md
ms.openlocfilehash: 03f898246b2f0d784725488f753697ed893b09df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917773"
---
# <span data-ttu-id="45dcb-101">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="45dcb-101">Set-AzVMADDomainExtension</span></span>

## <span data-ttu-id="45dcb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="45dcb-102">SYNOPSIS</span></span>
<span data-ttu-id="45dcb-103">新增 AD 網域擴充功能至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="45dcb-103">Adds an AD domain extension to a virtual machine.</span></span>

## <span data-ttu-id="45dcb-104">語法</span><span class="sxs-lookup"><span data-stu-id="45dcb-104">SYNTAX</span></span>

```
Set-AzVMADDomainExtension -DomainName <String> [-OUPath <String>] [-JoinOption <UInt32>]
 [-Credential <PSCredential>] [-Restart] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45dcb-105">描述</span><span class="sxs-lookup"><span data-stu-id="45dcb-105">DESCRIPTION</span></span>
<span data-ttu-id="45dcb-106">**Set-AzDOMADDomainExtension** Cmdlet 會將 Azure Active Directory (AD) 網域虛擬機器擴充功能新增到虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="45dcb-106">The **Set-AzVMADDomainExtension** cmdlet adds an Azure Active Directory (AD) domain virtual machine extension to a virtual machine.</span></span>
<span data-ttu-id="45dcb-107">此擴充功能可讓您的虛擬機器加入網域。</span><span class="sxs-lookup"><span data-stu-id="45dcb-107">This extension lets your virtual machine join a domain.</span></span>

## <span data-ttu-id="45dcb-108">例子</span><span class="sxs-lookup"><span data-stu-id="45dcb-108">EXAMPLES</span></span>

## <span data-ttu-id="45dcb-109">參數</span><span class="sxs-lookup"><span data-stu-id="45dcb-109">PARAMETERS</span></span>

### <span data-ttu-id="45dcb-110">-認證</span><span class="sxs-lookup"><span data-stu-id="45dcb-110">-Credential</span></span>
<span data-ttu-id="45dcb-111">將虛擬機器的使用者名稱和密碼指定為 **PSCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="45dcb-111">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="45dcb-112">若要取得認證，請使用 Get-Credential Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="45dcb-112">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="45dcb-113">如需要詳細資訊，請鍵入 `Get-Help Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="45dcb-113">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="45dcb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45dcb-114">-DefaultProfile</span></span>
<span data-ttu-id="45dcb-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="45dcb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45dcb-116">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="45dcb-116">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="45dcb-117">表示此 Cmdlet 會停用擴充功能次要版本的自動升級。</span><span class="sxs-lookup"><span data-stu-id="45dcb-117">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="45dcb-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="45dcb-118">-DomainName</span></span>
<span data-ttu-id="45dcb-119">指定網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="45dcb-119">Specifies the name of the domain.</span></span>

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

### <span data-ttu-id="45dcb-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="45dcb-120">-ForceRerun</span></span>
<span data-ttu-id="45dcb-121">表示此 Cmdlet 強制在虛擬機器上重新進行相同的擴充功能組配置，而不需要卸載並重新安裝擴充功能。</span><span class="sxs-lookup"><span data-stu-id="45dcb-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="45dcb-122">該值可以是與目前值不同的任何字串。</span><span class="sxs-lookup"><span data-stu-id="45dcb-122">The value can be any string different from the current value.</span></span>
<span data-ttu-id="45dcb-123">如果未變更 forceUpdateTag，處理常式仍然會使用公用或受保護的設定更新。</span><span class="sxs-lookup"><span data-stu-id="45dcb-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="45dcb-124">-JoinOption</span><span class="sxs-lookup"><span data-stu-id="45dcb-124">-JoinOption</span></span>
<span data-ttu-id="45dcb-125">指定連接選項。</span><span class="sxs-lookup"><span data-stu-id="45dcb-125">Specifies the join option.</span></span> <span data-ttu-id="45dcb-126">有關連接選項， [請參閱 fJoinOptions](https://docs.microsoft.com/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span><span class="sxs-lookup"><span data-stu-id="45dcb-126">For join options see [fJoinOptions](https://docs.microsoft.com/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain)</span></span>

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

### <span data-ttu-id="45dcb-127">-位置</span><span class="sxs-lookup"><span data-stu-id="45dcb-127">-Location</span></span>
<span data-ttu-id="45dcb-128">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="45dcb-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="45dcb-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="45dcb-129">-Name</span></span>
<span data-ttu-id="45dcb-130">指定要新增的網域副檔名。</span><span class="sxs-lookup"><span data-stu-id="45dcb-130">Specifies the name of the domain extension to add.</span></span>

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

### <span data-ttu-id="45dcb-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="45dcb-131">-NoWait</span></span>
<span data-ttu-id="45dcb-132">啟動作業，並立即在作業完成之前返回。</span><span class="sxs-lookup"><span data-stu-id="45dcb-132">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="45dcb-133">若要判斷作業是否成功完成，請使用一些其他機制。</span><span class="sxs-lookup"><span data-stu-id="45dcb-133">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="45dcb-134">-OUPath</span><span class="sxs-lookup"><span data-stu-id="45dcb-134">-OUPath</span></span>
<span data-ttu-id="45dcb-135">指定網域帳戶 (OU) 單位。</span><span class="sxs-lookup"><span data-stu-id="45dcb-135">Specifies an organizational unit (OU) for the domain account.</span></span>
<span data-ttu-id="45dcb-136">以引號輸入 OU 的完整區別名稱。</span><span class="sxs-lookup"><span data-stu-id="45dcb-136">Enter the full distinguished name of the OU in quotation marks.</span></span>
<span data-ttu-id="45dcb-137">預設值是網域中電腦物件的預設 OU。</span><span class="sxs-lookup"><span data-stu-id="45dcb-137">The default value is the default OU for machine objects in the domain.</span></span>

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

### <span data-ttu-id="45dcb-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45dcb-138">-ResourceGroupName</span></span>
<span data-ttu-id="45dcb-139">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="45dcb-139">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="45dcb-140">-重新開機</span><span class="sxs-lookup"><span data-stu-id="45dcb-140">-Restart</span></span>
<span data-ttu-id="45dcb-141">表示此 Cmdlet 會重新開機虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="45dcb-141">Indicates that this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="45dcb-142">經常需要重新開機，才能讓變更生效。</span><span class="sxs-lookup"><span data-stu-id="45dcb-142">A restart is often required to make the change effective.</span></span>

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

### <span data-ttu-id="45dcb-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="45dcb-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="45dcb-144">指定網域副檔名的版本。</span><span class="sxs-lookup"><span data-stu-id="45dcb-144">Specifies the version of the domain extension.</span></span>

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

### <span data-ttu-id="45dcb-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="45dcb-145">-VMName</span></span>
<span data-ttu-id="45dcb-146">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="45dcb-146">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="45dcb-147">-確認</span><span class="sxs-lookup"><span data-stu-id="45dcb-147">-Confirm</span></span>
<span data-ttu-id="45dcb-148">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="45dcb-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45dcb-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45dcb-149">-WhatIf</span></span>
<span data-ttu-id="45dcb-150">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="45dcb-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45dcb-151">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="45dcb-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45dcb-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45dcb-152">CommonParameters</span></span>
<span data-ttu-id="45dcb-153">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="45dcb-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45dcb-154">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45dcb-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45dcb-155">輸入</span><span class="sxs-lookup"><span data-stu-id="45dcb-155">INPUTS</span></span>

### <span data-ttu-id="45dcb-156">System.String</span><span class="sxs-lookup"><span data-stu-id="45dcb-156">System.String</span></span>

### <span data-ttu-id="45dcb-157">System.Nullable'1[[System.UInt32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="45dcb-157">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="45dcb-158">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="45dcb-158">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="45dcb-159">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="45dcb-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="45dcb-160">輸出</span><span class="sxs-lookup"><span data-stu-id="45dcb-160">OUTPUTS</span></span>

### <span data-ttu-id="45dcb-161">Microsoft.Azure.Commands.Compute.models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="45dcb-161">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="45dcb-162">筆記</span><span class="sxs-lookup"><span data-stu-id="45dcb-162">NOTES</span></span>

## <span data-ttu-id="45dcb-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="45dcb-163">RELATED LINKS</span></span>

[<span data-ttu-id="45dcb-164">Get-AzDOMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="45dcb-164">Get-AzVMADDomainExtension</span></span>](./Get-AzVMADDomainExtension.md)

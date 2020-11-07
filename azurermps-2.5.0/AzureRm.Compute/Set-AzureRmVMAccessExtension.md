---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaccessextension
schema: 2.0.0
ms.openlocfilehash: 069b98f585d606ade255cfecd223be4a074d8316
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801341"
---
# <span data-ttu-id="6c1d0-101">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="6c1d0-101">Set-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="6c1d0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6c1d0-102">SYNOPSIS</span></span>
<span data-ttu-id="6c1d0-103">將 VMAccess 延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6c1d0-103">Adds the VMAccess extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c1d0-104">句法</span><span class="sxs-lookup"><span data-stu-id="6c1d0-104">SYNTAX</span></span>

```
Set-AzureRmVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c1d0-105">說明</span><span class="sxs-lookup"><span data-stu-id="6c1d0-105">DESCRIPTION</span></span>
<span data-ttu-id="6c1d0-106">**AzureRmVMAccessExtension** Cmdlet 會將虛擬機器存取 (VMAccess) 虛擬電腦 VMAccess 擴展新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6c1d0-106">The **Set-AzureRmVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="6c1d0-107">VMAccess 延伸可以用來設定暫時的密碼，而且應該在登入電腦後立即變更它。</span><span class="sxs-lookup"><span data-stu-id="6c1d0-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span>

## <span data-ttu-id="6c1d0-108">示例</span><span class="sxs-lookup"><span data-stu-id="6c1d0-108">EXAMPLES</span></span>

### <span data-ttu-id="6c1d0-109">範例1：新增 VMAccess 延伸</span><span class="sxs-lookup"><span data-stu-id="6c1d0-109">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzureRmVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="6c1d0-110">這個命令會在 ResrouceGroup11 中為名為 VirtualMachine07 的虛擬機器新增 VMAccess 延伸。</span><span class="sxs-lookup"><span data-stu-id="6c1d0-110">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="6c1d0-111">此命令會指定 VMAccess 的 name 和 type 處理常式版本。</span><span class="sxs-lookup"><span data-stu-id="6c1d0-111">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="6c1d0-112">參數</span><span class="sxs-lookup"><span data-stu-id="6c1d0-112">PARAMETERS</span></span>

### <span data-ttu-id="6c1d0-113">-認證</span><span class="sxs-lookup"><span data-stu-id="6c1d0-113">-Credential</span></span>
<span data-ttu-id="6c1d0-114">指定虛擬機器的使用者名稱和密碼作為 **PSCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="6c1d0-114">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="6c1d0-115">若要取得認證，請使用 Get-Credential Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c1d0-115">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="6c1d0-116">如需詳細資訊，請輸入 `Get-Help Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="6c1d0-116">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="6c1d0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c1d0-117">-DefaultProfile</span></span>
<span data-ttu-id="6c1d0-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6c1d0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c1d0-119">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="6c1d0-119">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="6c1d0-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="6c1d0-120">-ForceRerun</span></span>
<span data-ttu-id="6c1d0-121">表示此 Cmdlet 會強制在虛擬機器上重新執行相同的延伸設定，而不需卸載並重新安裝延伸。</span><span class="sxs-lookup"><span data-stu-id="6c1d0-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="6c1d0-122">這個值可以是與目前值不同的任何字串。</span><span class="sxs-lookup"><span data-stu-id="6c1d0-122">The value can be any string different from the current value.</span></span>

<span data-ttu-id="6c1d0-123">如果 forceUpdateTag 未變更，處理常式仍會套用公用或受保護設定的更新。</span><span class="sxs-lookup"><span data-stu-id="6c1d0-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="6c1d0-124">-位置</span><span class="sxs-lookup"><span data-stu-id="6c1d0-124">-Location</span></span>
<span data-ttu-id="6c1d0-125">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="6c1d0-125">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="6c1d0-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="6c1d0-126">-Name</span></span>
<span data-ttu-id="6c1d0-127">指定此 Cmdlet 所新增之延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c1d0-127">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="6c1d0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c1d0-128">-ResourceGroupName</span></span>
<span data-ttu-id="6c1d0-129">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c1d0-129">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="6c1d0-130">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="6c1d0-130">-TypeHandlerVersion</span></span>
<span data-ttu-id="6c1d0-131">指定此虛擬機器要使用的副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="6c1d0-131">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="6c1d0-132">若要取得版本，請使用 Microsoft 的值來執行 Get-AzureRmVMExtensionImage Cmdlet。針對 *PublisherName* 參數和 VMAccessAgent （針對 *Type* 參數）進行計算。</span><span class="sxs-lookup"><span data-stu-id="6c1d0-132">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="6c1d0-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="6c1d0-133">-VMName</span></span>
<span data-ttu-id="6c1d0-134">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c1d0-134">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="6c1d0-135">這個 Cmdlet 會為此參數指定的虛擬機器新增 VMAccess。</span><span class="sxs-lookup"><span data-stu-id="6c1d0-135">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="6c1d0-136">-確認</span><span class="sxs-lookup"><span data-stu-id="6c1d0-136">-Confirm</span></span>
<span data-ttu-id="6c1d0-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6c1d0-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c1d0-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c1d0-138">-WhatIf</span></span>
<span data-ttu-id="6c1d0-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6c1d0-139">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="6c1d0-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c1d0-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c1d0-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c1d0-141">CommonParameters</span></span>
<span data-ttu-id="6c1d0-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6c1d0-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c1d0-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6c1d0-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c1d0-144">輸入</span><span class="sxs-lookup"><span data-stu-id="6c1d0-144">INPUTS</span></span>

### <span data-ttu-id="6c1d0-145">所有</span><span class="sxs-lookup"><span data-stu-id="6c1d0-145">None</span></span>
<span data-ttu-id="6c1d0-146">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="6c1d0-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6c1d0-147">輸出</span><span class="sxs-lookup"><span data-stu-id="6c1d0-147">OUTPUTS</span></span>

### <span data-ttu-id="6c1d0-148">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="6c1d0-148">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="6c1d0-149">筆記</span><span class="sxs-lookup"><span data-stu-id="6c1d0-149">NOTES</span></span>

## <span data-ttu-id="6c1d0-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="6c1d0-150">RELATED LINKS</span></span>

[<span data-ttu-id="6c1d0-151">AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="6c1d0-151">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="6c1d0-152">移除-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="6c1d0-152">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="6c1d0-153">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="6c1d0-153">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)

[<span data-ttu-id="6c1d0-154">AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="6c1d0-154">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)



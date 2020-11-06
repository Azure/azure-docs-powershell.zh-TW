---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmbginfoextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMBginfoExtension.md
ms.openlocfilehash: ac2a4e4e7d05aa23a5870f8a07ded2c7a43fcdae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445648"
---
# <span data-ttu-id="7c1e3-101">Set-AzureRmVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="7c1e3-101">Set-AzureRmVMBginfoExtension</span></span>

## <span data-ttu-id="7c1e3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7c1e3-102">SYNOPSIS</span></span>
<span data-ttu-id="7c1e3-103">將 BGInfo 延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="7c1e3-103">Adds the BGInfo extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c1e3-104">句法</span><span class="sxs-lookup"><span data-stu-id="7c1e3-104">SYNTAX</span></span>

```
Set-AzureRmVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c1e3-105">說明</span><span class="sxs-lookup"><span data-stu-id="7c1e3-105">DESCRIPTION</span></span>
<span data-ttu-id="7c1e3-106">**AzureRmVMBGInfoExtension** Cmdlet 會將 BGInfo 延伸新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="7c1e3-106">The **Set-AzureRmVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="7c1e3-107">示例</span><span class="sxs-lookup"><span data-stu-id="7c1e3-107">EXAMPLES</span></span>

### <span data-ttu-id="7c1e3-108">範例1：為虛擬機器新增 BGInfo 延伸</span><span class="sxs-lookup"><span data-stu-id="7c1e3-108">Example 1: Add the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzureRmVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="7c1e3-109">這個命令會將 BGInfo 延伸新增到名為 ContosoVM 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="7c1e3-109">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="7c1e3-110">命令會指定虛擬機器的資源群組和位置。</span><span class="sxs-lookup"><span data-stu-id="7c1e3-110">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="7c1e3-111">該命令會指定延伸的名稱和版本。</span><span class="sxs-lookup"><span data-stu-id="7c1e3-111">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="7c1e3-112">參數</span><span class="sxs-lookup"><span data-stu-id="7c1e3-112">PARAMETERS</span></span>

### <span data-ttu-id="7c1e3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c1e3-113">-DefaultProfile</span></span>
<span data-ttu-id="7c1e3-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7c1e3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c1e3-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="7c1e3-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="7c1e3-116">表示此 Cmdlet 可防止 Azure 來賓代理程式自動將延伸更新為較新的次要版本。</span><span class="sxs-lookup"><span data-stu-id="7c1e3-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="7c1e3-117">根據預設，這個 Cmdlet 可讓來賓代理程式更新延伸。</span><span class="sxs-lookup"><span data-stu-id="7c1e3-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

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

### <span data-ttu-id="7c1e3-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="7c1e3-118">-ForceRerun</span></span>
<span data-ttu-id="7c1e3-119">指定應該使用相同的公用或受保護設定來再次執行延伸。</span><span class="sxs-lookup"><span data-stu-id="7c1e3-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="7c1e3-120">這個值可以是與目前值不同的任何字串。</span><span class="sxs-lookup"><span data-stu-id="7c1e3-120">The value can be any string different from the current value.</span></span>
<span data-ttu-id="7c1e3-121">如果 forceUpdateTag 未變更，處理常式仍會套用公用或受保護設定的更新。</span><span class="sxs-lookup"><span data-stu-id="7c1e3-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="7c1e3-122">-位置</span><span class="sxs-lookup"><span data-stu-id="7c1e3-122">-Location</span></span>
<span data-ttu-id="7c1e3-123">指定虛擬機器的位置。</span><span class="sxs-lookup"><span data-stu-id="7c1e3-123">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="7c1e3-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="7c1e3-124">-Name</span></span>
<span data-ttu-id="7c1e3-125">指定此 Cmdlet 新增至虛擬機器之 BGInfo 延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c1e3-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

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

### <span data-ttu-id="7c1e3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c1e3-126">-ResourceGroupName</span></span>
<span data-ttu-id="7c1e3-127">指定此 Cmdlet 新增副檔名的虛擬機器資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c1e3-127">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

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

### <span data-ttu-id="7c1e3-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="7c1e3-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="7c1e3-129">指定此 Cmdlet 新增至虛擬機器的延伸版本。</span><span class="sxs-lookup"><span data-stu-id="7c1e3-129">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

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

### <span data-ttu-id="7c1e3-130">-VMName</span><span class="sxs-lookup"><span data-stu-id="7c1e3-130">-VMName</span></span>
<span data-ttu-id="7c1e3-131">指定此 Cmdlet 新增 BGInfo 延伸的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="7c1e3-131">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

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

### <span data-ttu-id="7c1e3-132">-確認</span><span class="sxs-lookup"><span data-stu-id="7c1e3-132">-Confirm</span></span>
<span data-ttu-id="7c1e3-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7c1e3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c1e3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c1e3-134">-WhatIf</span></span>
<span data-ttu-id="7c1e3-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7c1e3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c1e3-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7c1e3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c1e3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c1e3-137">CommonParameters</span></span>
<span data-ttu-id="7c1e3-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7c1e3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c1e3-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7c1e3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c1e3-140">輸入</span><span class="sxs-lookup"><span data-stu-id="7c1e3-140">INPUTS</span></span>

### <span data-ttu-id="7c1e3-141">System.object</span><span class="sxs-lookup"><span data-stu-id="7c1e3-141">System.String</span></span>

### <span data-ttu-id="7c1e3-142">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="7c1e3-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7c1e3-143">輸出</span><span class="sxs-lookup"><span data-stu-id="7c1e3-143">OUTPUTS</span></span>

### <span data-ttu-id="7c1e3-144">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="7c1e3-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="7c1e3-145">筆記</span><span class="sxs-lookup"><span data-stu-id="7c1e3-145">NOTES</span></span>

## <span data-ttu-id="7c1e3-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="7c1e3-146">RELATED LINKS</span></span>
---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9C216103-EB77-468E-8684-F5E5400B73A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsssshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssSshPublicKey.md
ms.openlocfilehash: de1cee534afa765c84cd20f4932b859cca8a71a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451887"
---
# <span data-ttu-id="66951-101">Add-AzureRmVmssSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="66951-101">Add-AzureRmVmssSshPublicKey</span></span>

## <span data-ttu-id="66951-102">摘要</span><span class="sxs-lookup"><span data-stu-id="66951-102">SYNOPSIS</span></span>
<span data-ttu-id="66951-103">將 SSH 公開金鑰新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="66951-103">Adds SSH public keys to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66951-104">句法</span><span class="sxs-lookup"><span data-stu-id="66951-104">SYNTAX</span></span>

```
Add-AzureRmVmssSshPublicKey [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Path] <String>]
 [[-KeyData] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66951-105">說明</span><span class="sxs-lookup"><span data-stu-id="66951-105">DESCRIPTION</span></span>
<span data-ttu-id="66951-106">**AzureRmVmssSshPublicKey** Cmdlet 會新增公開金鑰，您可以用來連線到 [虛擬機器] 規模集 () VMSS，透過安全 SHELL (SSH) 來連線至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="66951-106">The **Add-AzureRmVmssSshPublicKey** cmdlet adds the public keys that you can use to connect to the Virtual Machine Scale Set (VMSS) virtual machines over Secure Shell (SSH).</span></span>

## <span data-ttu-id="66951-107">示例</span><span class="sxs-lookup"><span data-stu-id="66951-107">EXAMPLES</span></span>

### <span data-ttu-id="66951-108">範例1：將 SSH 公開金鑰新增至 VMSS</span><span class="sxs-lookup"><span data-stu-id="66951-108">Example 1: Add an SSH public key to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSshPublicKey -VirtualMachineScaleSet $VMSS -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="66951-109">這個範例會將 SSH 公開金鑰新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="66951-109">This example adds an SSH public key to the VMSS.</span></span>
<span data-ttu-id="66951-110">第一個命令使用 **新的 AzureRmVmssConfig** Cmdlet 來建立 VMSS 設定物件，並將結果儲存在名為 $VMSS 的變數中。</span><span class="sxs-lookup"><span data-stu-id="66951-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="66951-111">第二個命令會將 SSH 金鑰與指定的金鑰資料相加，並將金鑰儲存在虛擬機器上的指定路徑中。</span><span class="sxs-lookup"><span data-stu-id="66951-111">The second command adds an SSH key with the specified key data and stores the key at the specified path on the virtual machine.</span></span>

## <span data-ttu-id="66951-112">參數</span><span class="sxs-lookup"><span data-stu-id="66951-112">PARAMETERS</span></span>

### <span data-ttu-id="66951-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66951-113">-DefaultProfile</span></span>
<span data-ttu-id="66951-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="66951-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66951-115">-KeyData</span><span class="sxs-lookup"><span data-stu-id="66951-115">-KeyData</span></span>
<span data-ttu-id="66951-116">指定 SSH RSA 公用金鑰資料。</span><span class="sxs-lookup"><span data-stu-id="66951-116">Specifies a SSH RSA public key data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66951-117">-Path</span><span class="sxs-lookup"><span data-stu-id="66951-117">-Path</span></span>
<span data-ttu-id="66951-118">指定檔案在虛擬機器上的完整路徑，此 Cmdlet 會儲存 SSH 公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="66951-118">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="66951-119">如果檔案已存在，此 Cmdlet 會將金鑰附加到檔案中。</span><span class="sxs-lookup"><span data-stu-id="66951-119">If the file already exists, this cmdlet appends the key to the file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66951-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="66951-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="66951-121">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="66951-121">Specifies the VMSS object.</span></span>
<span data-ttu-id="66951-122">您可以使用 [新的-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="66951-122">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66951-123">-確認</span><span class="sxs-lookup"><span data-stu-id="66951-123">-Confirm</span></span>
<span data-ttu-id="66951-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="66951-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66951-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66951-125">-WhatIf</span></span>
<span data-ttu-id="66951-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="66951-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="66951-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="66951-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66951-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66951-128">CommonParameters</span></span>
<span data-ttu-id="66951-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="66951-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66951-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="66951-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66951-131">輸入</span><span class="sxs-lookup"><span data-stu-id="66951-131">INPUTS</span></span>

### <span data-ttu-id="66951-132">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="66951-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="66951-133">System.object</span><span class="sxs-lookup"><span data-stu-id="66951-133">System.String</span></span>

## <span data-ttu-id="66951-134">輸出</span><span class="sxs-lookup"><span data-stu-id="66951-134">OUTPUTS</span></span>

### <span data-ttu-id="66951-135">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="66951-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="66951-136">筆記</span><span class="sxs-lookup"><span data-stu-id="66951-136">NOTES</span></span>

## <span data-ttu-id="66951-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="66951-137">RELATED LINKS</span></span>

[<span data-ttu-id="66951-138">新-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="66951-138">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
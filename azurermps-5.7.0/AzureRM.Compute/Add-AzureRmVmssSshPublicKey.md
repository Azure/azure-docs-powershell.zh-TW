---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9C216103-EB77-468E-8684-F5E5400B73A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSshPublicKey.md
ms.openlocfilehash: 6ca619ba75fcf639e36650dc66d45d2f86ec8375
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625933"
---
# <span data-ttu-id="da10c-101">Add-AzureRmVmssSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="da10c-101">Add-AzureRmVmssSshPublicKey</span></span>

## <span data-ttu-id="da10c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="da10c-102">SYNOPSIS</span></span>
<span data-ttu-id="da10c-103">將 SSH 公開金鑰新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="da10c-103">Adds SSH public keys to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da10c-104">句法</span><span class="sxs-lookup"><span data-stu-id="da10c-104">SYNTAX</span></span>

```
Add-AzureRmVmssSshPublicKey [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Path] <String>]
 [[-KeyData] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da10c-105">說明</span><span class="sxs-lookup"><span data-stu-id="da10c-105">DESCRIPTION</span></span>
<span data-ttu-id="da10c-106">**AzureRmVmssSshPublicKey** Cmdlet 會新增公開金鑰，您可以用來連線到 [虛擬機器] 規模集 () VMSS，透過安全 SHELL (SSH) 來連線至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="da10c-106">The **Add-AzureRmVmssSshPublicKey** cmdlet adds the public keys that you can use to connect to the Virtual Machine Scale Set (VMSS) virtual machines over Secure Shell (SSH).</span></span>

## <span data-ttu-id="da10c-107">示例</span><span class="sxs-lookup"><span data-stu-id="da10c-107">EXAMPLES</span></span>

### <span data-ttu-id="da10c-108">範例1：將 SSH 公開金鑰新增至 VMSS</span><span class="sxs-lookup"><span data-stu-id="da10c-108">Example 1: Add an SSH public key to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSshPublicKey -VirtualMachineScaleSet $VMSS -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="da10c-109">這個範例會將 SSH 公開金鑰新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="da10c-109">This example adds an SSH public key to the VMSS.</span></span>

<span data-ttu-id="da10c-110">第一個命令使用 **新的 AzureRmVmssConfig** Cmdlet 來建立 VMSS 設定物件，並將結果儲存在名為 $VMSS 的變數中。</span><span class="sxs-lookup"><span data-stu-id="da10c-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="da10c-111">第二個命令會將 SSH 金鑰與指定的金鑰資料相加，並將金鑰儲存在虛擬機器上的指定路徑中。</span><span class="sxs-lookup"><span data-stu-id="da10c-111">The second command adds an SSH key with the specified key data and stores the key at the specified path on the virtual machine.</span></span>

## <span data-ttu-id="da10c-112">參數</span><span class="sxs-lookup"><span data-stu-id="da10c-112">PARAMETERS</span></span>

### <span data-ttu-id="da10c-113">-KeyData</span><span class="sxs-lookup"><span data-stu-id="da10c-113">-KeyData</span></span>
<span data-ttu-id="da10c-114">指定 SSH RSA 公用金鑰資料。</span><span class="sxs-lookup"><span data-stu-id="da10c-114">Specifies a SSH RSA public key data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da10c-115">-Path</span><span class="sxs-lookup"><span data-stu-id="da10c-115">-Path</span></span>
<span data-ttu-id="da10c-116">指定檔案在虛擬機器上的完整路徑，此 Cmdlet 會儲存 SSH 公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="da10c-116">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="da10c-117">如果檔案已存在，此 Cmdlet 會將金鑰附加到檔案中。</span><span class="sxs-lookup"><span data-stu-id="da10c-117">If the file already exists, this cmdlet appends the key to the file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da10c-118">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="da10c-118">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="da10c-119">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="da10c-119">Specifies the VMSS object.</span></span>
<span data-ttu-id="da10c-120">您可以使用 [新的-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="da10c-120">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da10c-121">-確認</span><span class="sxs-lookup"><span data-stu-id="da10c-121">-Confirm</span></span>
<span data-ttu-id="da10c-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="da10c-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da10c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da10c-123">-WhatIf</span></span>
<span data-ttu-id="da10c-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="da10c-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da10c-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="da10c-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da10c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da10c-126">CommonParameters</span></span>
<span data-ttu-id="da10c-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="da10c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da10c-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="da10c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da10c-129">輸入</span><span class="sxs-lookup"><span data-stu-id="da10c-129">INPUTS</span></span>

### <span data-ttu-id="da10c-130">所有</span><span class="sxs-lookup"><span data-stu-id="da10c-130">None</span></span>
<span data-ttu-id="da10c-131">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="da10c-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="da10c-132">輸出</span><span class="sxs-lookup"><span data-stu-id="da10c-132">OUTPUTS</span></span>

###  
<span data-ttu-id="da10c-133">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="da10c-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="da10c-134">筆記</span><span class="sxs-lookup"><span data-stu-id="da10c-134">NOTES</span></span>

## <span data-ttu-id="da10c-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="da10c-135">RELATED LINKS</span></span>

[<span data-ttu-id="da10c-136">新-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="da10c-136">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)

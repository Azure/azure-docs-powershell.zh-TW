---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 9C216103-EB77-468E-8684-F5E5400B73A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssSshPublicKey.md
ms.openlocfilehash: 2fb8d5956cf783940e32f49019115dd911050749
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796358"
---
# <span data-ttu-id="07f1b-101">Add-AzVmssSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="07f1b-101">Add-AzVmssSshPublicKey</span></span>

## <span data-ttu-id="07f1b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="07f1b-102">SYNOPSIS</span></span>
<span data-ttu-id="07f1b-103">將 SSH 公開金鑰新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="07f1b-103">Adds SSH public keys to the VMSS.</span></span>

## <span data-ttu-id="07f1b-104">句法</span><span class="sxs-lookup"><span data-stu-id="07f1b-104">SYNTAX</span></span>

```
Add-AzVmssSshPublicKey [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Path] <String>]
 [[-KeyData] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07f1b-105">說明</span><span class="sxs-lookup"><span data-stu-id="07f1b-105">DESCRIPTION</span></span>
<span data-ttu-id="07f1b-106">**AzVmssSshPublicKey** Cmdlet 會新增公開金鑰，您可以用來連線到 [虛擬機器] 規模集 () VMSS，透過安全 SHELL (SSH) 來連線至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="07f1b-106">The **Add-AzVmssSshPublicKey** cmdlet adds the public keys that you can use to connect to the Virtual Machine Scale Set (VMSS) virtual machines over Secure Shell (SSH).</span></span>

## <span data-ttu-id="07f1b-107">示例</span><span class="sxs-lookup"><span data-stu-id="07f1b-107">EXAMPLES</span></span>

### <span data-ttu-id="07f1b-108">範例1：將 SSH 公開金鑰新增至 VMSS</span><span class="sxs-lookup"><span data-stu-id="07f1b-108">Example 1: Add an SSH public key to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSshPublicKey -VirtualMachineScaleSet $VMSS -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="07f1b-109">這個範例會將 SSH 公開金鑰新增至 VMSS。</span><span class="sxs-lookup"><span data-stu-id="07f1b-109">This example adds an SSH public key to the VMSS.</span></span>

<span data-ttu-id="07f1b-110">第一個命令使用 **新的 AzVmssConfig** Cmdlet 來建立 VMSS 設定物件，並將結果儲存在名為 $VMSS 的變數中。</span><span class="sxs-lookup"><span data-stu-id="07f1b-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="07f1b-111">第二個命令會將 SSH 金鑰與指定的金鑰資料相加，並將金鑰儲存在虛擬機器上的指定路徑中。</span><span class="sxs-lookup"><span data-stu-id="07f1b-111">The second command adds an SSH key with the specified key data and stores the key at the specified path on the virtual machine.</span></span>

## <span data-ttu-id="07f1b-112">參數</span><span class="sxs-lookup"><span data-stu-id="07f1b-112">PARAMETERS</span></span>

### <span data-ttu-id="07f1b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07f1b-113">-DefaultProfile</span></span>
<span data-ttu-id="07f1b-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="07f1b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07f1b-115">-KeyData</span><span class="sxs-lookup"><span data-stu-id="07f1b-115">-KeyData</span></span>
<span data-ttu-id="07f1b-116">指定 SSH RSA 公用金鑰資料。</span><span class="sxs-lookup"><span data-stu-id="07f1b-116">Specifies a SSH RSA public key data.</span></span>

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

### <span data-ttu-id="07f1b-117">-Path</span><span class="sxs-lookup"><span data-stu-id="07f1b-117">-Path</span></span>
<span data-ttu-id="07f1b-118">指定檔案在虛擬機器上的完整路徑，此 Cmdlet 會儲存 SSH 公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="07f1b-118">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="07f1b-119">如果檔案已存在，此 Cmdlet 會將金鑰附加到檔案中。</span><span class="sxs-lookup"><span data-stu-id="07f1b-119">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="07f1b-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="07f1b-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="07f1b-121">指定 VMSS 物件。</span><span class="sxs-lookup"><span data-stu-id="07f1b-121">Specifies the VMSS object.</span></span>
<span data-ttu-id="07f1b-122">您可以使用 [新的-AzVmssConfig](./New-AzVmssConfig.md) Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="07f1b-122">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07f1b-123">-確認</span><span class="sxs-lookup"><span data-stu-id="07f1b-123">-Confirm</span></span>
<span data-ttu-id="07f1b-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="07f1b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07f1b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07f1b-125">-WhatIf</span></span>
<span data-ttu-id="07f1b-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="07f1b-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07f1b-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="07f1b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07f1b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07f1b-128">CommonParameters</span></span>
<span data-ttu-id="07f1b-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="07f1b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07f1b-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="07f1b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07f1b-131">輸入</span><span class="sxs-lookup"><span data-stu-id="07f1b-131">INPUTS</span></span>

### <span data-ttu-id="07f1b-132">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="07f1b-132">VirtualMachineScaleSet</span></span>
<span data-ttu-id="07f1b-133">形參 "VirtualMachineScaleSet" 接受管線中 "VirtualMachineScaleSet" 類型的值</span><span class="sxs-lookup"><span data-stu-id="07f1b-133">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="07f1b-134">輸出</span><span class="sxs-lookup"><span data-stu-id="07f1b-134">OUTPUTS</span></span>

###  
<span data-ttu-id="07f1b-135">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="07f1b-135">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="07f1b-136">筆記</span><span class="sxs-lookup"><span data-stu-id="07f1b-136">NOTES</span></span>

## <span data-ttu-id="07f1b-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="07f1b-137">RELATED LINKS</span></span>

[<span data-ttu-id="07f1b-138">新-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="07f1b-138">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
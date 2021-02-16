---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: e17b495147c308d20d6d5b950914d26ce56a5706
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138691"
---
# <span data-ttu-id="54e45-101">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="54e45-101">Add-AzVMSshPublicKey</span></span>

## <span data-ttu-id="54e45-102">摘要</span><span class="sxs-lookup"><span data-stu-id="54e45-102">SYNOPSIS</span></span>
<span data-ttu-id="54e45-103">只要建立 VM，就會為虛擬機器新增 SSH 的公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="54e45-103">Adds the public keys for SSH for a virtual machine, when only creating the VM.</span></span>

## <span data-ttu-id="54e45-104">句法</span><span class="sxs-lookup"><span data-stu-id="54e45-104">SYNTAX</span></span>

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54e45-105">說明</span><span class="sxs-lookup"><span data-stu-id="54e45-105">DESCRIPTION</span></span>
<span data-ttu-id="54e45-106">**AzVMSshPublicKey** Cmdlet 會新增您可以用來透過安全 Shell 連線至 Linux 虛擬機器的公開金鑰， (SSH) ]。</span><span class="sxs-lookup"><span data-stu-id="54e45-106">The **Add-AzVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a Linux virtual machine over Secure Shell (SSH).</span></span> <span data-ttu-id="54e45-107">在建立 VM 之後，如果您嘗試在建立 vm 之後使用此命令，不需要更新-AzVM，就不會發生錯誤，如果您使用含有 Update-AzVM 的命令，命令就會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="54e45-107">This cannot be used after VM creation, if you try to use this after VM creation without Update-AzVM, there will be no error, if you use the command with Update-AzVM, the command will error.</span></span>

## <span data-ttu-id="54e45-108">示例</span><span class="sxs-lookup"><span data-stu-id="54e45-108">EXAMPLES</span></span>

### <span data-ttu-id="54e45-109">範例1：將公開金鑰新增至虛擬機器</span><span class="sxs-lookup"><span data-stu-id="54e45-109">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="54e45-110">第一個命令會使用 **AzVM** Cmdlet 取得名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="54e45-110">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="54e45-111">該命令會將虛擬機器儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="54e45-111">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="54e45-112">第二個命令會將公開金鑰新增到 VirtualMachine07 中 Path 參數指定的位置。</span><span class="sxs-lookup"><span data-stu-id="54e45-112">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="54e45-113">參數</span><span class="sxs-lookup"><span data-stu-id="54e45-113">PARAMETERS</span></span>

### <span data-ttu-id="54e45-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54e45-114">-DefaultProfile</span></span>
<span data-ttu-id="54e45-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="54e45-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54e45-116">-KeyData</span><span class="sxs-lookup"><span data-stu-id="54e45-116">-KeyData</span></span>
<span data-ttu-id="54e45-117">指定公用金鑰的基本64編碼。</span><span class="sxs-lookup"><span data-stu-id="54e45-117">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="54e45-118">您可以使用 SSH 或使用此參數指定的金鑰連線至 Linux 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="54e45-118">You can connect to a Linux virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="54e45-119">-Path</span><span class="sxs-lookup"><span data-stu-id="54e45-119">-Path</span></span>
<span data-ttu-id="54e45-120">指定檔案在虛擬機器上的完整路徑，此 Cmdlet 會儲存 SSH 公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="54e45-120">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="54e45-121">如果檔案已存在，此 Cmdlet 會將金鑰附加到檔案中。</span><span class="sxs-lookup"><span data-stu-id="54e45-121">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="54e45-122">-VM</span><span class="sxs-lookup"><span data-stu-id="54e45-122">-VM</span></span>
<span data-ttu-id="54e45-123">指定此 Cmdlet 修改的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="54e45-123">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="54e45-124">若要取得虛擬機器物件，請使用 [AzVM](./Get-AzVM.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="54e45-124">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="54e45-125">您可以使用 [新的 AzVMConfig](./New-AzVMConfig.md) Cmdlet 來建立虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="54e45-125">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54e45-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54e45-126">CommonParameters</span></span>
<span data-ttu-id="54e45-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="54e45-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54e45-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="54e45-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54e45-129">輸入</span><span class="sxs-lookup"><span data-stu-id="54e45-129">INPUTS</span></span>

### <span data-ttu-id="54e45-130">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="54e45-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="54e45-131">System.object</span><span class="sxs-lookup"><span data-stu-id="54e45-131">System.String</span></span>

## <span data-ttu-id="54e45-132">輸出</span><span class="sxs-lookup"><span data-stu-id="54e45-132">OUTPUTS</span></span>

### <span data-ttu-id="54e45-133">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="54e45-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="54e45-134">筆記</span><span class="sxs-lookup"><span data-stu-id="54e45-134">NOTES</span></span>

## <span data-ttu-id="54e45-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="54e45-135">RELATED LINKS</span></span>

[<span data-ttu-id="54e45-136">AzVM</span><span class="sxs-lookup"><span data-stu-id="54e45-136">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="54e45-137">新-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="54e45-137">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

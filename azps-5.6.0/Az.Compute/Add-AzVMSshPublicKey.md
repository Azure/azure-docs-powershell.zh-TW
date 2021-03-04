---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: 4c6d2b3376bb5e92d048db61d68c7cfb1b94ee01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909201"
---
# <span data-ttu-id="88b13-101">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="88b13-101">Add-AzVMSshPublicKey</span></span>

## <span data-ttu-id="88b13-102">簡介</span><span class="sxs-lookup"><span data-stu-id="88b13-102">SYNOPSIS</span></span>
<span data-ttu-id="88b13-103">在僅建立 VM 時，新增虛擬機器 SSH 的公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="88b13-103">Adds the public keys for SSH for a virtual machine, when only creating the VM.</span></span>

## <span data-ttu-id="88b13-104">語法</span><span class="sxs-lookup"><span data-stu-id="88b13-104">SYNTAX</span></span>

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88b13-105">描述</span><span class="sxs-lookup"><span data-stu-id="88b13-105">DESCRIPTION</span></span>
<span data-ttu-id="88b13-106">**Add-AzMSshPublicKey Cmdlet** 會新增您可用於在 Secure Shell (SSH) 上連接至 Linux 虛擬機器的公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="88b13-106">The **Add-AzVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a Linux virtual machine over Secure Shell (SSH).</span></span> <span data-ttu-id="88b13-107">建立 VM 之後，就無法使用此功能，如果您在建立 VM 後嘗試使用這個命令，而不使用 Update-Az VM，則沒有錯誤;如果您使用 Update-Az VM 命令，則命令會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="88b13-107">This cannot be used after VM creation, if you try to use this after VM creation without Update-AzVM, there will be no error, if you use the command with Update-AzVM, the command will error.</span></span>

## <span data-ttu-id="88b13-108">例子</span><span class="sxs-lookup"><span data-stu-id="88b13-108">EXAMPLES</span></span>

### <span data-ttu-id="88b13-109">範例 1：新增公開金鑰至虛擬機器</span><span class="sxs-lookup"><span data-stu-id="88b13-109">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="88b13-110">第一個命令會使用 **Get-Az VIRTUAL** Cmdlet 取得名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="88b13-110">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="88b13-111">該命令將虛擬機器儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="88b13-111">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="88b13-112">第二個命令會將公開金鑰新增到 VirtualMachine07 上 Path 參數指定的位置。</span><span class="sxs-lookup"><span data-stu-id="88b13-112">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="88b13-113">參數</span><span class="sxs-lookup"><span data-stu-id="88b13-113">PARAMETERS</span></span>

### <span data-ttu-id="88b13-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88b13-114">-DefaultProfile</span></span>
<span data-ttu-id="88b13-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="88b13-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88b13-116">-KeyData</span><span class="sxs-lookup"><span data-stu-id="88b13-116">-KeyData</span></span>
<span data-ttu-id="88b13-117">指定公用鍵的底數 64 編碼。</span><span class="sxs-lookup"><span data-stu-id="88b13-117">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="88b13-118">您可以使用 SSH 或此參數指定的金鑰來連接到 Linux 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="88b13-118">You can connect to a Linux virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="88b13-119">-路徑</span><span class="sxs-lookup"><span data-stu-id="88b13-119">-Path</span></span>
<span data-ttu-id="88b13-120">指定檔案的完整路徑，位於此 Cmdlet 儲存 SSH 公開金鑰的虛擬機器上。</span><span class="sxs-lookup"><span data-stu-id="88b13-120">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="88b13-121">如果檔案已存在，此 Cmdlet 會附加該金鑰至檔案。</span><span class="sxs-lookup"><span data-stu-id="88b13-121">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="88b13-122">-VM</span><span class="sxs-lookup"><span data-stu-id="88b13-122">-VM</span></span>
<span data-ttu-id="88b13-123">指定此 Cmdlet 修改的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="88b13-123">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="88b13-124">若要取得虛擬機器物件，請使用[Get-Az%。CMdlet。](./Get-AzVM.md)</span><span class="sxs-lookup"><span data-stu-id="88b13-124">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="88b13-125">您可以使用 [New-AzMSConfig](./New-AzVMConfig.md) Cmdlet 來建立虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="88b13-125">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="88b13-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88b13-126">CommonParameters</span></span>
<span data-ttu-id="88b13-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="88b13-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88b13-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88b13-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88b13-129">輸入</span><span class="sxs-lookup"><span data-stu-id="88b13-129">INPUTS</span></span>

### <span data-ttu-id="88b13-130">Microsoft.Azure.Commands.Compute.models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="88b13-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="88b13-131">System.String</span><span class="sxs-lookup"><span data-stu-id="88b13-131">System.String</span></span>

## <span data-ttu-id="88b13-132">輸出</span><span class="sxs-lookup"><span data-stu-id="88b13-132">OUTPUTS</span></span>

### <span data-ttu-id="88b13-133">Microsoft.Azure.Commands.Compute.models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="88b13-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="88b13-134">筆記</span><span class="sxs-lookup"><span data-stu-id="88b13-134">NOTES</span></span>

## <span data-ttu-id="88b13-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="88b13-135">RELATED LINKS</span></span>

[<span data-ttu-id="88b13-136">Get-AzMS</span><span class="sxs-lookup"><span data-stu-id="88b13-136">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="88b13-137">New-AzMSCONFIG</span><span class="sxs-lookup"><span data-stu-id="88b13-137">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

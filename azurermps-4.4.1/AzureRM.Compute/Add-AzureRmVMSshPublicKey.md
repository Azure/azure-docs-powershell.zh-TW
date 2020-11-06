---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
ms.openlocfilehash: 24c97e73728dab656a1d9fe3283e4eba6aae4ea2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445128"
---
# <span data-ttu-id="46184-101">Add-AzureRmVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="46184-101">Add-AzureRmVMSshPublicKey</span></span>

## <span data-ttu-id="46184-102">摘要</span><span class="sxs-lookup"><span data-stu-id="46184-102">SYNOPSIS</span></span>
<span data-ttu-id="46184-103">為虛擬機器新增 SSH 的公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="46184-103">Adds the public keys for SSH for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46184-104">句法</span><span class="sxs-lookup"><span data-stu-id="46184-104">SYNTAX</span></span>

```
Add-AzureRmVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46184-105">說明</span><span class="sxs-lookup"><span data-stu-id="46184-105">DESCRIPTION</span></span>
<span data-ttu-id="46184-106">**AzureRmVMSshPublicKey** Cmdlet 會新增您可以用來透過安全 Shell 連線至虛擬機器的公開金鑰， (SSH) ]。</span><span class="sxs-lookup"><span data-stu-id="46184-106">The **Add-AzureRmVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a virtual machine over Secure Shell (SSH).</span></span>

## <span data-ttu-id="46184-107">示例</span><span class="sxs-lookup"><span data-stu-id="46184-107">EXAMPLES</span></span>

### <span data-ttu-id="46184-108">範例1：將公開金鑰新增至虛擬機器</span><span class="sxs-lookup"><span data-stu-id="46184-108">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzureRmVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="46184-109">第一個命令會使用 **AzureRmVM** Cmdlet 取得名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="46184-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="46184-110">該命令會將虛擬機器儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="46184-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="46184-111">第二個命令會將公開金鑰新增到 VirtualMachine07 中 Path 參數指定的位置。</span><span class="sxs-lookup"><span data-stu-id="46184-111">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="46184-112">參數</span><span class="sxs-lookup"><span data-stu-id="46184-112">PARAMETERS</span></span>

### <span data-ttu-id="46184-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46184-113">-DefaultProfile</span></span>
<span data-ttu-id="46184-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="46184-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46184-115">-KeyData</span><span class="sxs-lookup"><span data-stu-id="46184-115">-KeyData</span></span>
<span data-ttu-id="46184-116">指定公用金鑰的基本64編碼。</span><span class="sxs-lookup"><span data-stu-id="46184-116">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="46184-117">您可以使用 SSH 或使用此參數指定的金鑰連線到虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="46184-117">You can connect to a virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="46184-118">-Path</span><span class="sxs-lookup"><span data-stu-id="46184-118">-Path</span></span>
<span data-ttu-id="46184-119">指定檔案在虛擬機器上的完整路徑，此 Cmdlet 會儲存 SSH 公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="46184-119">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="46184-120">如果檔案已存在，此 Cmdlet 會將金鑰附加到檔案中。</span><span class="sxs-lookup"><span data-stu-id="46184-120">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="46184-121">-VM</span><span class="sxs-lookup"><span data-stu-id="46184-121">-VM</span></span>
<span data-ttu-id="46184-122">指定此 Cmdlet 修改的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="46184-122">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="46184-123">若要取得虛擬機器物件，請使用 [AzureRmVM](./Get-AzureRmVM.md) Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46184-123">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="46184-124">您可以使用 [新的 AzureRmVMConfig](./New-AzureRmVMConfig.md) Cmdlet 來建立虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="46184-124">You can use the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="46184-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46184-125">CommonParameters</span></span>
<span data-ttu-id="46184-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="46184-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46184-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="46184-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46184-128">輸入</span><span class="sxs-lookup"><span data-stu-id="46184-128">INPUTS</span></span>

## <span data-ttu-id="46184-129">輸出</span><span class="sxs-lookup"><span data-stu-id="46184-129">OUTPUTS</span></span>

## <span data-ttu-id="46184-130">筆記</span><span class="sxs-lookup"><span data-stu-id="46184-130">NOTES</span></span>

## <span data-ttu-id="46184-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="46184-131">RELATED LINKS</span></span>

[<span data-ttu-id="46184-132">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="46184-132">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="46184-133">新-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="46184-133">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
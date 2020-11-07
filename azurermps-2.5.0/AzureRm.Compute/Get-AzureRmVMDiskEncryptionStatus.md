---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdiskencryptionstatus
schema: 2.0.0
ms.openlocfilehash: 667ebae58974b2dc68d19daa6a4f3a9d2e98075d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93799989"
---
# <span data-ttu-id="388a8-101">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="388a8-101">Get-AzureRmVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="388a8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="388a8-102">SYNOPSIS</span></span>
<span data-ttu-id="388a8-103">取得虛擬機器的加密狀態。</span><span class="sxs-lookup"><span data-stu-id="388a8-103">Gets the encryption status of the virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="388a8-104">句法</span><span class="sxs-lookup"><span data-stu-id="388a8-104">SYNTAX</span></span>

```
Get-AzureRmVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="388a8-105">說明</span><span class="sxs-lookup"><span data-stu-id="388a8-105">DESCRIPTION</span></span>
<span data-ttu-id="388a8-106">**AzureRmVMDiskEncryptionStatus** Cmdlet 會取得虛擬機器的加密狀態。</span><span class="sxs-lookup"><span data-stu-id="388a8-106">The **Get-AzureRmVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="388a8-107">它會顯示作業系統和資料量的加密狀態。</span><span class="sxs-lookup"><span data-stu-id="388a8-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="388a8-108">除了加密狀態之外，它也會顯示加密機密 URL、金鑰加密金鑰 URL、作業系統的加密金鑰和金鑰加密金鑰的 **KeyVaults** 。</span><span class="sxs-lookup"><span data-stu-id="388a8-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="388a8-109">示例</span><span class="sxs-lookup"><span data-stu-id="388a8-109">EXAMPLES</span></span>

### <span data-ttu-id="388a8-110">範例1：取得虛擬機器的加密狀態</span><span class="sxs-lookup"><span data-stu-id="388a8-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzureRmVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="388a8-111">這個命令會取得名為 VM001 的虛擬機器的加密狀態。</span><span class="sxs-lookup"><span data-stu-id="388a8-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="388a8-112">參數</span><span class="sxs-lookup"><span data-stu-id="388a8-112">PARAMETERS</span></span>

### <span data-ttu-id="388a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="388a8-113">-DefaultProfile</span></span>
<span data-ttu-id="388a8-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="388a8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="388a8-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="388a8-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="388a8-116">延伸發行者名稱。</span><span class="sxs-lookup"><span data-stu-id="388a8-116">The extension publisher name.</span></span> <span data-ttu-id="388a8-117">指定此參數，只會覆寫「Microsoft Azure. Security」的預設值。</span><span class="sxs-lookup"><span data-stu-id="388a8-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="388a8-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="388a8-118">-ExtensionType</span></span>
<span data-ttu-id="388a8-119">延伸類型。</span><span class="sxs-lookup"><span data-stu-id="388a8-119">The extension type.</span></span> <span data-ttu-id="388a8-120">指定此參數可覆寫 Windows Vm 的 "AzureDiskEncryption" 的預設值，以及 Linux Vm 的 "AzureDiskEncryptionForLinux"。</span><span class="sxs-lookup"><span data-stu-id="388a8-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="388a8-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="388a8-121">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="388a8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="388a8-122">-ResourceGroupName</span></span>
<span data-ttu-id="388a8-123">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="388a8-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="388a8-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="388a8-124">-VMName</span></span>
<span data-ttu-id="388a8-125">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="388a8-125">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="388a8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="388a8-126">CommonParameters</span></span>
<span data-ttu-id="388a8-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="388a8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="388a8-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="388a8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="388a8-129">輸入</span><span class="sxs-lookup"><span data-stu-id="388a8-129">INPUTS</span></span>

### <span data-ttu-id="388a8-130">所有</span><span class="sxs-lookup"><span data-stu-id="388a8-130">None</span></span>
<span data-ttu-id="388a8-131">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="388a8-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="388a8-132">輸出</span><span class="sxs-lookup"><span data-stu-id="388a8-132">OUTPUTS</span></span>

### <span data-ttu-id="388a8-133">AzureDiskEncryptionExtensionCoNtext 中的 AzureDiskEncryption 的副檔名。</span><span class="sxs-lookup"><span data-stu-id="388a8-133">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="388a8-134">筆記</span><span class="sxs-lookup"><span data-stu-id="388a8-134">NOTES</span></span>

## <span data-ttu-id="388a8-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="388a8-135">RELATED LINKS</span></span>

[<span data-ttu-id="388a8-136">移除-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="388a8-136">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="388a8-137">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="388a8-137">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)



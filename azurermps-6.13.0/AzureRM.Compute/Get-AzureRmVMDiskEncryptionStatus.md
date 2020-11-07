---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdiskencryptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
ms.openlocfilehash: b208d7c0e0db028f1b3242a70be508fbbc3788ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624907"
---
# <span data-ttu-id="94c3d-101">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="94c3d-101">Get-AzureRmVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="94c3d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="94c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="94c3d-103">取得虛擬機器的加密狀態。</span><span class="sxs-lookup"><span data-stu-id="94c3d-103">Gets the encryption status of the virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94c3d-104">句法</span><span class="sxs-lookup"><span data-stu-id="94c3d-104">SYNTAX</span></span>

```
Get-AzureRmVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94c3d-105">說明</span><span class="sxs-lookup"><span data-stu-id="94c3d-105">DESCRIPTION</span></span>
<span data-ttu-id="94c3d-106">**AzureRmVMDiskEncryptionStatus** Cmdlet 會取得虛擬機器的加密狀態。</span><span class="sxs-lookup"><span data-stu-id="94c3d-106">The **Get-AzureRmVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="94c3d-107">它會顯示作業系統和資料量的加密狀態。</span><span class="sxs-lookup"><span data-stu-id="94c3d-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="94c3d-108">除了加密狀態之外，它也會顯示加密機密 URL、金鑰加密金鑰 URL、作業系統的加密金鑰和金鑰加密金鑰的 **KeyVaults** 。</span><span class="sxs-lookup"><span data-stu-id="94c3d-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="94c3d-109">示例</span><span class="sxs-lookup"><span data-stu-id="94c3d-109">EXAMPLES</span></span>

### <span data-ttu-id="94c3d-110">範例1：取得虛擬機器的加密狀態</span><span class="sxs-lookup"><span data-stu-id="94c3d-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzureRmVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="94c3d-111">這個命令會取得名為 VM001 的虛擬機器的加密狀態。</span><span class="sxs-lookup"><span data-stu-id="94c3d-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="94c3d-112">參數</span><span class="sxs-lookup"><span data-stu-id="94c3d-112">PARAMETERS</span></span>

### <span data-ttu-id="94c3d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94c3d-113">-DefaultProfile</span></span>
<span data-ttu-id="94c3d-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="94c3d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94c3d-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="94c3d-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="94c3d-116">延伸發行者名稱。</span><span class="sxs-lookup"><span data-stu-id="94c3d-116">The extension publisher name.</span></span> <span data-ttu-id="94c3d-117">指定此參數，只會覆寫「Microsoft Azure. Security」的預設值。</span><span class="sxs-lookup"><span data-stu-id="94c3d-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="94c3d-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="94c3d-118">-ExtensionType</span></span>
<span data-ttu-id="94c3d-119">延伸類型。</span><span class="sxs-lookup"><span data-stu-id="94c3d-119">The extension type.</span></span> <span data-ttu-id="94c3d-120">指定此參數可覆寫 Windows Vm 的 "AzureDiskEncryption" 的預設值，以及 Linux Vm 的 "AzureDiskEncryptionForLinux"。</span><span class="sxs-lookup"><span data-stu-id="94c3d-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="94c3d-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="94c3d-121">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94c3d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94c3d-122">-ResourceGroupName</span></span>
<span data-ttu-id="94c3d-123">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="94c3d-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="94c3d-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="94c3d-124">-VMName</span></span>
<span data-ttu-id="94c3d-125">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="94c3d-125">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="94c3d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94c3d-126">CommonParameters</span></span>
<span data-ttu-id="94c3d-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="94c3d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94c3d-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="94c3d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94c3d-129">輸入</span><span class="sxs-lookup"><span data-stu-id="94c3d-129">INPUTS</span></span>

### <span data-ttu-id="94c3d-130">System.object</span><span class="sxs-lookup"><span data-stu-id="94c3d-130">System.String</span></span>

## <span data-ttu-id="94c3d-131">輸出</span><span class="sxs-lookup"><span data-stu-id="94c3d-131">OUTPUTS</span></span>

### <span data-ttu-id="94c3d-132">AzureDiskEncryptionExtensionCoNtext 中的 AzureDiskEncryption 的副檔名。</span><span class="sxs-lookup"><span data-stu-id="94c3d-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="94c3d-133">筆記</span><span class="sxs-lookup"><span data-stu-id="94c3d-133">NOTES</span></span>

## <span data-ttu-id="94c3d-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="94c3d-134">RELATED LINKS</span></span>

[<span data-ttu-id="94c3d-135">移除-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="94c3d-135">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="94c3d-136">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="94c3d-136">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)



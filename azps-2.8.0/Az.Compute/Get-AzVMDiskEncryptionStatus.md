---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiskencryptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
ms.openlocfilehash: 1b2a3855703c1d91a17cfd164f6a65ce218da486
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613383"
---
# <span data-ttu-id="1d274-101">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="1d274-101">Get-AzVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="1d274-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1d274-102">SYNOPSIS</span></span>
<span data-ttu-id="1d274-103">取得虛擬機器的加密狀態。</span><span class="sxs-lookup"><span data-stu-id="1d274-103">Gets the encryption status of the virtual machine.</span></span>

## <span data-ttu-id="1d274-104">句法</span><span class="sxs-lookup"><span data-stu-id="1d274-104">SYNTAX</span></span>

```
Get-AzVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1d274-105">說明</span><span class="sxs-lookup"><span data-stu-id="1d274-105">DESCRIPTION</span></span>
<span data-ttu-id="1d274-106">**AzVMDiskEncryptionStatus** Cmdlet 會取得虛擬機器的加密狀態。</span><span class="sxs-lookup"><span data-stu-id="1d274-106">The **Get-AzVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="1d274-107">它會顯示作業系統和資料量的加密狀態。</span><span class="sxs-lookup"><span data-stu-id="1d274-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="1d274-108">除了加密狀態之外，它也會顯示加密機密 URL、金鑰加密金鑰 URL、作業系統的加密金鑰和金鑰加密金鑰的 **KeyVaults** 。</span><span class="sxs-lookup"><span data-stu-id="1d274-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="1d274-109">示例</span><span class="sxs-lookup"><span data-stu-id="1d274-109">EXAMPLES</span></span>

### <span data-ttu-id="1d274-110">範例1：取得虛擬機器的加密狀態</span><span class="sxs-lookup"><span data-stu-id="1d274-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="1d274-111">這個命令會取得名為 VM001 的虛擬機器的加密狀態。</span><span class="sxs-lookup"><span data-stu-id="1d274-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="1d274-112">參數</span><span class="sxs-lookup"><span data-stu-id="1d274-112">PARAMETERS</span></span>

### <span data-ttu-id="1d274-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d274-113">-DefaultProfile</span></span>
<span data-ttu-id="1d274-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1d274-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d274-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="1d274-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="1d274-116">延伸發行者名稱。</span><span class="sxs-lookup"><span data-stu-id="1d274-116">The extension publisher name.</span></span> <span data-ttu-id="1d274-117">指定此參數，只會覆寫「Microsoft Azure. Security」的預設值。</span><span class="sxs-lookup"><span data-stu-id="1d274-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="1d274-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="1d274-118">-ExtensionType</span></span>
<span data-ttu-id="1d274-119">延伸類型。</span><span class="sxs-lookup"><span data-stu-id="1d274-119">The extension type.</span></span> <span data-ttu-id="1d274-120">指定此參數可覆寫 Windows Vm 的 "AzureDiskEncryption" 的預設值，以及 Linux Vm 的 "AzureDiskEncryptionForLinux"。</span><span class="sxs-lookup"><span data-stu-id="1d274-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="1d274-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="1d274-121">-Name</span></span>
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

### <span data-ttu-id="1d274-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d274-122">-ResourceGroupName</span></span>
<span data-ttu-id="1d274-123">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1d274-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1d274-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="1d274-124">-VMName</span></span>
<span data-ttu-id="1d274-125">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="1d274-125">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="1d274-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d274-126">CommonParameters</span></span>
<span data-ttu-id="1d274-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1d274-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d274-128">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1d274-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d274-129">輸入</span><span class="sxs-lookup"><span data-stu-id="1d274-129">INPUTS</span></span>

### <span data-ttu-id="1d274-130">System.object</span><span class="sxs-lookup"><span data-stu-id="1d274-130">System.String</span></span>

## <span data-ttu-id="1d274-131">輸出</span><span class="sxs-lookup"><span data-stu-id="1d274-131">OUTPUTS</span></span>

### <span data-ttu-id="1d274-132">AzureDiskEncryptionExtensionCoNtext 中的 AzureDiskEncryption 的副檔名。</span><span class="sxs-lookup"><span data-stu-id="1d274-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="1d274-133">筆記</span><span class="sxs-lookup"><span data-stu-id="1d274-133">NOTES</span></span>

## <span data-ttu-id="1d274-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="1d274-134">RELATED LINKS</span></span>

[<span data-ttu-id="1d274-135">移除-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="1d274-135">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="1d274-136">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="1d274-136">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


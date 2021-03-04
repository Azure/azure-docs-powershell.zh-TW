---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmdiskencryptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
ms.openlocfilehash: 7d0a7537594bb41fbcc41a7ddf457820c9b29dd1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909174"
---
# <span data-ttu-id="f0ba4-101">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="f0ba4-101">Get-AzVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="f0ba4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f0ba4-102">SYNOPSIS</span></span>
<span data-ttu-id="f0ba4-103">獲得虛擬機器的加密狀態。</span><span class="sxs-lookup"><span data-stu-id="f0ba4-103">Gets the encryption status of the virtual machine.</span></span>

## <span data-ttu-id="f0ba4-104">語法</span><span class="sxs-lookup"><span data-stu-id="f0ba4-104">SYNTAX</span></span>

```
Get-AzVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f0ba4-105">描述</span><span class="sxs-lookup"><span data-stu-id="f0ba4-105">DESCRIPTION</span></span>
<span data-ttu-id="f0ba4-106">**Get-Az VIRTUALCryptEncryptionStatus** Cmdlet 會取得虛擬機器的加密狀態。</span><span class="sxs-lookup"><span data-stu-id="f0ba4-106">The **Get-AzVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="f0ba4-107">它會顯示作業系統和資料量的加密狀態。</span><span class="sxs-lookup"><span data-stu-id="f0ba4-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="f0ba4-108">除了加密狀態之外，它也會顯示加密金鑰 URL、金鑰加密金鑰 **URL、KeyVaults 的資源識別碼，** 其中會顯示作業系統音量的加密金鑰和金鑰加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="f0ba4-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="f0ba4-109">例子</span><span class="sxs-lookup"><span data-stu-id="f0ba4-109">EXAMPLES</span></span>

### <span data-ttu-id="f0ba4-110">範例 1：取得虛擬機器的加密狀態</span><span class="sxs-lookup"><span data-stu-id="f0ba4-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="f0ba4-111">此命令會獲得名為 VM001 之虛擬機器的加密狀態。</span><span class="sxs-lookup"><span data-stu-id="f0ba4-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="f0ba4-112">參數</span><span class="sxs-lookup"><span data-stu-id="f0ba4-112">PARAMETERS</span></span>

### <span data-ttu-id="f0ba4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0ba4-113">-DefaultProfile</span></span>
<span data-ttu-id="f0ba4-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f0ba4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0ba4-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="f0ba4-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="f0ba4-116">擴充功能發行者名稱。</span><span class="sxs-lookup"><span data-stu-id="f0ba4-116">The extension publisher name.</span></span> <span data-ttu-id="f0ba4-117">僅指定此參數以覆蓋 "Microsoft.Azure.Security" 的預設值。</span><span class="sxs-lookup"><span data-stu-id="f0ba4-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="f0ba4-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="f0ba4-118">-ExtensionType</span></span>
<span data-ttu-id="f0ba4-119">副檔名類型。</span><span class="sxs-lookup"><span data-stu-id="f0ba4-119">The extension type.</span></span> <span data-ttu-id="f0ba4-120">指定此參數以覆蓋其預設值 "AzureAzEncryption" for Windows VMs 和 "AzureCryptEncryptionForWindows" for Linux 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f0ba4-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="f0ba4-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="f0ba4-121">-Name</span></span>
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

### <span data-ttu-id="f0ba4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0ba4-122">-ResourceGroupName</span></span>
<span data-ttu-id="f0ba4-123">指定虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f0ba4-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f0ba4-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="f0ba4-124">-VMName</span></span>
<span data-ttu-id="f0ba4-125">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0ba4-125">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="f0ba4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0ba4-126">CommonParameters</span></span>
<span data-ttu-id="f0ba4-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f0ba4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0ba4-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0ba4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0ba4-129">輸入</span><span class="sxs-lookup"><span data-stu-id="f0ba4-129">INPUTS</span></span>

### <span data-ttu-id="f0ba4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f0ba4-130">System.String</span></span>

## <span data-ttu-id="f0ba4-131">輸出</span><span class="sxs-lookup"><span data-stu-id="f0ba4-131">OUTPUTS</span></span>

### <span data-ttu-id="f0ba4-132">Microsoft.Azure.Commands.Compute.Extension.AzureCryptEncryption.AzureTextEncryptionExtensionCoNtext</span><span class="sxs-lookup"><span data-stu-id="f0ba4-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="f0ba4-133">筆記</span><span class="sxs-lookup"><span data-stu-id="f0ba4-133">NOTES</span></span>

## <span data-ttu-id="f0ba4-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0ba4-134">RELATED LINKS</span></span>

[<span data-ttu-id="f0ba4-135">Remove-AzCRYPTCryptEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="f0ba4-135">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="f0ba4-136">Set-Az解說EncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="f0ba4-136">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)



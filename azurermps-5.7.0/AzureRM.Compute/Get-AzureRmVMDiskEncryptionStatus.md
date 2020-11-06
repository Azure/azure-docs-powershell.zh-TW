---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
ms.openlocfilehash: 9ec94d0c11bf9302156355c28566ce16f48ae148
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449399"
---
# <span data-ttu-id="b3f12-101">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="b3f12-101">Get-AzureRmVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="b3f12-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b3f12-102">SYNOPSIS</span></span>
<span data-ttu-id="b3f12-103">取得虛擬機器的加密狀態。</span><span class="sxs-lookup"><span data-stu-id="b3f12-103">Gets the encryption status of the virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3f12-104">句法</span><span class="sxs-lookup"><span data-stu-id="b3f12-104">SYNTAX</span></span>

```
Get-AzureRmVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3f12-105">說明</span><span class="sxs-lookup"><span data-stu-id="b3f12-105">DESCRIPTION</span></span>
<span data-ttu-id="b3f12-106">**AzureRmVMDiskEncryptionStatus** Cmdlet 會取得虛擬機器的加密狀態。</span><span class="sxs-lookup"><span data-stu-id="b3f12-106">The **Get-AzureRmVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="b3f12-107">它會顯示作業系統和資料量的加密狀態。</span><span class="sxs-lookup"><span data-stu-id="b3f12-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="b3f12-108">除了加密狀態之外，它也會顯示加密機密 URL、金鑰加密金鑰 URL、作業系統的加密金鑰和金鑰加密金鑰的 **KeyVaults** 。</span><span class="sxs-lookup"><span data-stu-id="b3f12-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="b3f12-109">示例</span><span class="sxs-lookup"><span data-stu-id="b3f12-109">EXAMPLES</span></span>

### <span data-ttu-id="b3f12-110">範例1：取得虛擬機器的加密狀態</span><span class="sxs-lookup"><span data-stu-id="b3f12-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzureRmVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="b3f12-111">這個命令會取得名為 VM001 的虛擬機器的加密狀態。</span><span class="sxs-lookup"><span data-stu-id="b3f12-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="b3f12-112">參數</span><span class="sxs-lookup"><span data-stu-id="b3f12-112">PARAMETERS</span></span>

### <span data-ttu-id="b3f12-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="b3f12-113">-Name</span></span>
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

### <span data-ttu-id="b3f12-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3f12-114">-ResourceGroupName</span></span>
<span data-ttu-id="b3f12-115">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3f12-115">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b3f12-116">-VMName</span><span class="sxs-lookup"><span data-stu-id="b3f12-116">-VMName</span></span>
<span data-ttu-id="b3f12-117">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3f12-117">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="b3f12-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3f12-118">CommonParameters</span></span>
<span data-ttu-id="b3f12-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b3f12-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3f12-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b3f12-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3f12-121">輸入</span><span class="sxs-lookup"><span data-stu-id="b3f12-121">INPUTS</span></span>

### <span data-ttu-id="b3f12-122">所有</span><span class="sxs-lookup"><span data-stu-id="b3f12-122">None</span></span>
<span data-ttu-id="b3f12-123">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="b3f12-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b3f12-124">輸出</span><span class="sxs-lookup"><span data-stu-id="b3f12-124">OUTPUTS</span></span>

## <span data-ttu-id="b3f12-125">筆記</span><span class="sxs-lookup"><span data-stu-id="b3f12-125">NOTES</span></span>

## <span data-ttu-id="b3f12-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3f12-126">RELATED LINKS</span></span>

[<span data-ttu-id="b3f12-127">移除-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="b3f12-127">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="b3f12-128">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="b3f12-128">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)



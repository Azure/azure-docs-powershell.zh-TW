---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
ms.openlocfilehash: 56fcbadbcdbd874df3fea74918381eb24b2fa1f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909149"
---
# <span data-ttu-id="f5a53-101">Get-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="f5a53-101">Get-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="f5a53-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f5a53-102">SYNOPSIS</span></span>
<span data-ttu-id="f5a53-103">顯示 VM 縮放集的磁片加密狀態。</span><span class="sxs-lookup"><span data-stu-id="f5a53-103">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="f5a53-104">語法</span><span class="sxs-lookup"><span data-stu-id="f5a53-104">SYNTAX</span></span>

```
Get-AzVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5a53-105">描述</span><span class="sxs-lookup"><span data-stu-id="f5a53-105">DESCRIPTION</span></span>
<span data-ttu-id="f5a53-106">顯示 VM 縮放集的磁片加密狀態。</span><span class="sxs-lookup"><span data-stu-id="f5a53-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="f5a53-107">例子</span><span class="sxs-lookup"><span data-stu-id="f5a53-107">EXAMPLES</span></span>

### <span data-ttu-id="f5a53-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="f5a53-108">Example 1</span></span>
```
PS C:\> Get-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="f5a53-109">顯示名稱為 VMSS001 的 VM 縮放集的磁片加密狀態，該集合屬於名為 Group001 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="f5a53-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="f5a53-110">參數</span><span class="sxs-lookup"><span data-stu-id="f5a53-110">PARAMETERS</span></span>

### <span data-ttu-id="f5a53-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5a53-111">-DefaultProfile</span></span>
<span data-ttu-id="f5a53-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f5a53-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5a53-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="f5a53-113">-ExtensionName</span></span>
<span data-ttu-id="f5a53-114">副檔名。</span><span class="sxs-lookup"><span data-stu-id="f5a53-114">The extension name.</span></span>
<span data-ttu-id="f5a53-115">如果未指定此參數，則使用的預設值為適用于 Windows VMs 的 AzureCryptEncryption，以及適用于 Linux VMs 的 AzureCryptEncryptionForWindows。</span><span class="sxs-lookup"><span data-stu-id="f5a53-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="f5a53-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5a53-116">-ResourceGroupName</span></span>
<span data-ttu-id="f5a53-117">虛擬機器縮放集的資源組名</span><span class="sxs-lookup"><span data-stu-id="f5a53-117">Resource group name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5a53-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f5a53-118">-VMScaleSetName</span></span>
<span data-ttu-id="f5a53-119">虛擬機器縮放比例集名稱。</span><span class="sxs-lookup"><span data-stu-id="f5a53-119">The virtual machine scale set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5a53-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5a53-120">CommonParameters</span></span>
<span data-ttu-id="f5a53-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f5a53-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5a53-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5a53-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5a53-123">輸入</span><span class="sxs-lookup"><span data-stu-id="f5a53-123">INPUTS</span></span>

### <span data-ttu-id="f5a53-124">System.String</span><span class="sxs-lookup"><span data-stu-id="f5a53-124">System.String</span></span>

## <span data-ttu-id="f5a53-125">輸出</span><span class="sxs-lookup"><span data-stu-id="f5a53-125">OUTPUTS</span></span>

### <span data-ttu-id="f5a53-126">Microsoft.Azure.Commands.Compute.models.PSEvsAzencryptionStatusCoNtext</span><span class="sxs-lookup"><span data-stu-id="f5a53-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="f5a53-127">筆記</span><span class="sxs-lookup"><span data-stu-id="f5a53-127">NOTES</span></span>

## <span data-ttu-id="f5a53-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5a53-128">RELATED LINKS</span></span>

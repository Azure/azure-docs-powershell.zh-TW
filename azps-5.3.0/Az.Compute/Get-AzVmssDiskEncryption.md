---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
ms.openlocfilehash: 5f47931817cf640349cd4d3226fe8ffa4819d259
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98446408"
---
# <span data-ttu-id="a9f21-101">Get-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="a9f21-101">Get-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="a9f21-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a9f21-102">SYNOPSIS</span></span>
<span data-ttu-id="a9f21-103">顯示 VM 比例集的磁片加密狀態。</span><span class="sxs-lookup"><span data-stu-id="a9f21-103">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="a9f21-104">句法</span><span class="sxs-lookup"><span data-stu-id="a9f21-104">SYNTAX</span></span>

```
Get-AzVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9f21-105">說明</span><span class="sxs-lookup"><span data-stu-id="a9f21-105">DESCRIPTION</span></span>
<span data-ttu-id="a9f21-106">顯示 VM 比例集的磁片加密狀態。</span><span class="sxs-lookup"><span data-stu-id="a9f21-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="a9f21-107">示例</span><span class="sxs-lookup"><span data-stu-id="a9f21-107">EXAMPLES</span></span>

### <span data-ttu-id="a9f21-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a9f21-108">Example 1</span></span>
```
PS C:\> Get-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="a9f21-109">顯示屬於名為 Group001 之資源群組且名為 VMSS001 之 VM 規模集的磁片加密狀態。</span><span class="sxs-lookup"><span data-stu-id="a9f21-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="a9f21-110">參數</span><span class="sxs-lookup"><span data-stu-id="a9f21-110">PARAMETERS</span></span>

### <span data-ttu-id="a9f21-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9f21-111">-DefaultProfile</span></span>
<span data-ttu-id="a9f21-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a9f21-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9f21-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="a9f21-113">-ExtensionName</span></span>
<span data-ttu-id="a9f21-114">副檔名。</span><span class="sxs-lookup"><span data-stu-id="a9f21-114">The extension name.</span></span>
<span data-ttu-id="a9f21-115">如果未指定此參數，則使用的預設值是適用于 windows Vm 的 AzureDiskEncryption，以及適用于 Linux Vm 的 AzureDiskEncryptionForLinux。</span><span class="sxs-lookup"><span data-stu-id="a9f21-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="a9f21-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9f21-116">-ResourceGroupName</span></span>
<span data-ttu-id="a9f21-117">虛擬機器規模集的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="a9f21-117">Resource group name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="a9f21-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a9f21-118">-VMScaleSetName</span></span>
<span data-ttu-id="a9f21-119">虛擬機器比例集名稱。</span><span class="sxs-lookup"><span data-stu-id="a9f21-119">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="a9f21-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9f21-120">CommonParameters</span></span>
<span data-ttu-id="a9f21-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a9f21-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9f21-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a9f21-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9f21-123">輸入</span><span class="sxs-lookup"><span data-stu-id="a9f21-123">INPUTS</span></span>

### <span data-ttu-id="a9f21-124">System.object</span><span class="sxs-lookup"><span data-stu-id="a9f21-124">System.String</span></span>

## <span data-ttu-id="a9f21-125">輸出</span><span class="sxs-lookup"><span data-stu-id="a9f21-125">OUTPUTS</span></span>

### <span data-ttu-id="a9f21-126">PSVmssDiskEncryptionStatusCoNtext 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="a9f21-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="a9f21-127">筆記</span><span class="sxs-lookup"><span data-stu-id="a9f21-127">NOTES</span></span>

## <span data-ttu-id="a9f21-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9f21-128">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
ms.openlocfilehash: a697ead2f971191d108d4fb348a213e35b363d63
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912905"
---
# <span data-ttu-id="f2c7e-101">Get-AzVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="f2c7e-101">Get-AzVmssVMDiskEncryption</span></span>

## <span data-ttu-id="f2c7e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f2c7e-102">SYNOPSIS</span></span>
<span data-ttu-id="f2c7e-103">顯示 VM 縮放集內虛擬機器的磁片加密狀態。</span><span class="sxs-lookup"><span data-stu-id="f2c7e-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

## <span data-ttu-id="f2c7e-104">語法</span><span class="sxs-lookup"><span data-stu-id="f2c7e-104">SYNTAX</span></span>

```
Get-AzVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String>]
 [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2c7e-105">描述</span><span class="sxs-lookup"><span data-stu-id="f2c7e-105">DESCRIPTION</span></span>
<span data-ttu-id="f2c7e-106">顯示 VM 縮放集的磁片加密狀態。</span><span class="sxs-lookup"><span data-stu-id="f2c7e-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="f2c7e-107">例子</span><span class="sxs-lookup"><span data-stu-id="f2c7e-107">EXAMPLES</span></span>

### <span data-ttu-id="f2c7e-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="f2c7e-108">Example 1</span></span>
```
PS C:\> Get-AzVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="f2c7e-109">顯示名稱為 VMSS001 之 VM 規模集的 VM 實例 1 的磁片加密狀態，此狀態屬於名為 Group001 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="f2c7e-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="f2c7e-110">參數</span><span class="sxs-lookup"><span data-stu-id="f2c7e-110">PARAMETERS</span></span>

### <span data-ttu-id="f2c7e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2c7e-111">-DefaultProfile</span></span>
<span data-ttu-id="f2c7e-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2c7e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2c7e-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="f2c7e-113">-ExtensionName</span></span>
<span data-ttu-id="f2c7e-114">副檔名。</span><span class="sxs-lookup"><span data-stu-id="f2c7e-114">The extension name.</span></span>
<span data-ttu-id="f2c7e-115">如果未指定此參數，則使用的預設值為適用于 Windows VMs 的 AzureCryptEncryption，以及適用于 Linux VMs 的 AzureCryptEncryptionForWindows。</span><span class="sxs-lookup"><span data-stu-id="f2c7e-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="f2c7e-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="f2c7e-116">-InstanceId</span></span>
<span data-ttu-id="f2c7e-117">指定實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="f2c7e-117">Specifies the instance ID.</span></span>

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

### <span data-ttu-id="f2c7e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2c7e-118">-ResourceGroupName</span></span>
<span data-ttu-id="f2c7e-119">虛擬機器縮放集的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f2c7e-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="f2c7e-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f2c7e-120">-VMScaleSetName</span></span>
<span data-ttu-id="f2c7e-121">虛擬機器縮放比例集名稱。</span><span class="sxs-lookup"><span data-stu-id="f2c7e-121">The virtual machine scale set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2c7e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2c7e-122">CommonParameters</span></span>
<span data-ttu-id="f2c7e-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f2c7e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2c7e-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2c7e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2c7e-125">輸入</span><span class="sxs-lookup"><span data-stu-id="f2c7e-125">INPUTS</span></span>

### <span data-ttu-id="f2c7e-126">System.String</span><span class="sxs-lookup"><span data-stu-id="f2c7e-126">System.String</span></span>

## <span data-ttu-id="f2c7e-127">輸出</span><span class="sxs-lookup"><span data-stu-id="f2c7e-127">OUTPUTS</span></span>

### <span data-ttu-id="f2c7e-128">Microsoft.Azure.Commands.Compute.models.PSEvsSVTCryptEncryptionStatusCoNtext</span><span class="sxs-lookup"><span data-stu-id="f2c7e-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="f2c7e-129">筆記</span><span class="sxs-lookup"><span data-stu-id="f2c7e-129">NOTES</span></span>

## <span data-ttu-id="f2c7e-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2c7e-130">RELATED LINKS</span></span>

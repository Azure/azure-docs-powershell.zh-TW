---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
ms.openlocfilehash: 8ff3ad92f976e6a8af9c4a24e143ed3859832d35
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127129"
---
# <span data-ttu-id="743bb-101">Get-AzVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="743bb-101">Get-AzVmssVMDiskEncryption</span></span>

## <span data-ttu-id="743bb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="743bb-102">SYNOPSIS</span></span>
<span data-ttu-id="743bb-103">顯示 VM 規模集中 Vm 的磁片加密狀態。</span><span class="sxs-lookup"><span data-stu-id="743bb-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

## <span data-ttu-id="743bb-104">句法</span><span class="sxs-lookup"><span data-stu-id="743bb-104">SYNTAX</span></span>

```
Get-AzVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String>]
 [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="743bb-105">說明</span><span class="sxs-lookup"><span data-stu-id="743bb-105">DESCRIPTION</span></span>
<span data-ttu-id="743bb-106">顯示 VM 比例集的磁片加密狀態。</span><span class="sxs-lookup"><span data-stu-id="743bb-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="743bb-107">示例</span><span class="sxs-lookup"><span data-stu-id="743bb-107">EXAMPLES</span></span>

### <span data-ttu-id="743bb-108">範例1</span><span class="sxs-lookup"><span data-stu-id="743bb-108">Example 1</span></span>
```
PS C:\> Get-AzVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="743bb-109">顯示屬於名為 Group001 之資源群組的 VM 實例1的磁片加密狀態（名為 VMSS001）。</span><span class="sxs-lookup"><span data-stu-id="743bb-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="743bb-110">參數</span><span class="sxs-lookup"><span data-stu-id="743bb-110">PARAMETERS</span></span>

### <span data-ttu-id="743bb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="743bb-111">-DefaultProfile</span></span>
<span data-ttu-id="743bb-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="743bb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="743bb-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="743bb-113">-ExtensionName</span></span>
<span data-ttu-id="743bb-114">副檔名。</span><span class="sxs-lookup"><span data-stu-id="743bb-114">The extension name.</span></span>
<span data-ttu-id="743bb-115">如果未指定此參數，則使用的預設值是適用于 windows Vm 的 AzureDiskEncryption，以及適用于 Linux Vm 的 AzureDiskEncryptionForLinux。</span><span class="sxs-lookup"><span data-stu-id="743bb-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="743bb-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="743bb-116">-InstanceId</span></span>
<span data-ttu-id="743bb-117">指定實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="743bb-117">Specifies the instance ID.</span></span>

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

### <span data-ttu-id="743bb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="743bb-118">-ResourceGroupName</span></span>
<span data-ttu-id="743bb-119">虛擬機器規模集的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="743bb-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="743bb-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="743bb-120">-VMScaleSetName</span></span>
<span data-ttu-id="743bb-121">虛擬機器比例集名稱。</span><span class="sxs-lookup"><span data-stu-id="743bb-121">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="743bb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="743bb-122">CommonParameters</span></span>
<span data-ttu-id="743bb-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="743bb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="743bb-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="743bb-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="743bb-125">輸入</span><span class="sxs-lookup"><span data-stu-id="743bb-125">INPUTS</span></span>

### <span data-ttu-id="743bb-126">System.object</span><span class="sxs-lookup"><span data-stu-id="743bb-126">System.String</span></span>

## <span data-ttu-id="743bb-127">輸出</span><span class="sxs-lookup"><span data-stu-id="743bb-127">OUTPUTS</span></span>

### <span data-ttu-id="743bb-128">PSVmssVMDiskEncryptionStatusCoNtext 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="743bb-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="743bb-129">筆記</span><span class="sxs-lookup"><span data-stu-id="743bb-129">NOTES</span></span>

## <span data-ttu-id="743bb-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="743bb-130">RELATED LINKS</span></span>

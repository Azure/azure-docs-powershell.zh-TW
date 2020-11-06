---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssVMDiskEncryption.md
ms.openlocfilehash: c45574272d814ea899e7d291b729b6a8e6526da6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446375"
---
# <span data-ttu-id="c0354-101">Get-AzureRmVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="c0354-101">Get-AzureRmVmssVMDiskEncryption</span></span>

## <span data-ttu-id="c0354-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c0354-102">SYNOPSIS</span></span>
<span data-ttu-id="c0354-103">顯示 VM 規模集中 Vm 的磁片加密狀態。</span><span class="sxs-lookup"><span data-stu-id="c0354-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0354-104">句法</span><span class="sxs-lookup"><span data-stu-id="c0354-104">SYNTAX</span></span>

```
Get-AzureRmVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-InstanceId] <String>] [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0354-105">說明</span><span class="sxs-lookup"><span data-stu-id="c0354-105">DESCRIPTION</span></span>
<span data-ttu-id="c0354-106">顯示 VM 比例集的磁片加密狀態。</span><span class="sxs-lookup"><span data-stu-id="c0354-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="c0354-107">示例</span><span class="sxs-lookup"><span data-stu-id="c0354-107">EXAMPLES</span></span>

### <span data-ttu-id="c0354-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c0354-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="c0354-109">顯示屬於名為 Group001 之資源群組的 VM 實例1的磁片加密狀態（名為 VMSS001）。</span><span class="sxs-lookup"><span data-stu-id="c0354-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="c0354-110">參數</span><span class="sxs-lookup"><span data-stu-id="c0354-110">PARAMETERS</span></span>

### <span data-ttu-id="c0354-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0354-111">-DefaultProfile</span></span>
<span data-ttu-id="c0354-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0354-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0354-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="c0354-113">-ExtensionName</span></span>
<span data-ttu-id="c0354-114">副檔名。</span><span class="sxs-lookup"><span data-stu-id="c0354-114">The extension name.</span></span>
<span data-ttu-id="c0354-115">如果未指定此參數，則使用的預設值是適用于 windows Vm 的 AzureDiskEncryption，以及適用于 Linux Vm 的 AzureDiskEncryptionForLinux。</span><span class="sxs-lookup"><span data-stu-id="c0354-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="c0354-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="c0354-116">-InstanceId</span></span>
<span data-ttu-id="c0354-117">指定實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="c0354-117">Specifies the instance ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0354-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0354-118">-ResourceGroupName</span></span>
<span data-ttu-id="c0354-119">虛擬機器規模集的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c0354-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="c0354-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c0354-120">-VMScaleSetName</span></span>
<span data-ttu-id="c0354-121">虛擬機器比例集名稱。</span><span class="sxs-lookup"><span data-stu-id="c0354-121">The virtual machine scale set name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0354-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0354-122">CommonParameters</span></span>
<span data-ttu-id="c0354-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c0354-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0354-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c0354-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0354-125">輸入</span><span class="sxs-lookup"><span data-stu-id="c0354-125">INPUTS</span></span>

### <span data-ttu-id="c0354-126">System.object</span><span class="sxs-lookup"><span data-stu-id="c0354-126">System.String</span></span>

## <span data-ttu-id="c0354-127">輸出</span><span class="sxs-lookup"><span data-stu-id="c0354-127">OUTPUTS</span></span>

### <span data-ttu-id="c0354-128">PSVmssVMDiskEncryptionStatusCoNtext 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="c0354-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="c0354-129">筆記</span><span class="sxs-lookup"><span data-stu-id="c0354-129">NOTES</span></span>

## <span data-ttu-id="c0354-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0354-130">RELATED LINKS</span></span>

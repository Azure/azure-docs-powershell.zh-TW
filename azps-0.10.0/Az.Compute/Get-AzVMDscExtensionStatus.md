---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextensionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
ms.openlocfilehash: 3ae9827c6db5136b9327936a63ac0441dcf94ff1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796246"
---
# <span data-ttu-id="c9e76-101">Get-AzVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="c9e76-101">Get-AzVMDscExtensionStatus</span></span>

## <span data-ttu-id="c9e76-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c9e76-102">SYNOPSIS</span></span>
<span data-ttu-id="c9e76-103">取得虛擬機器的 DSC 延伸處理常式狀態。</span><span class="sxs-lookup"><span data-stu-id="c9e76-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

## <span data-ttu-id="c9e76-104">句法</span><span class="sxs-lookup"><span data-stu-id="c9e76-104">SYNTAX</span></span>

```
Get-AzVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9e76-105">說明</span><span class="sxs-lookup"><span data-stu-id="c9e76-105">DESCRIPTION</span></span>
<span data-ttu-id="c9e76-106">AzVMDscExtensionStatus Cmdlet 會針對資源群組中的虛擬機器， **取得** 所需狀態配置 (DSC) 延伸處理常式的狀態設定。</span><span class="sxs-lookup"><span data-stu-id="c9e76-106">The **Get-AzVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="c9e76-107">套用配置時，此 Cmdlet 會產生與 Start-DscConfiguration Cmdlet 一致的輸出。</span><span class="sxs-lookup"><span data-stu-id="c9e76-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="c9e76-108">示例</span><span class="sxs-lookup"><span data-stu-id="c9e76-108">EXAMPLES</span></span>

### <span data-ttu-id="c9e76-109">sr-1</span><span class="sxs-lookup"><span data-stu-id="c9e76-109">1:</span></span>
```

```

## <span data-ttu-id="c9e76-110">參數</span><span class="sxs-lookup"><span data-stu-id="c9e76-110">PARAMETERS</span></span>

### <span data-ttu-id="c9e76-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9e76-111">-DefaultProfile</span></span>
<span data-ttu-id="c9e76-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c9e76-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9e76-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="c9e76-113">-Name</span></span>
<span data-ttu-id="c9e76-114">指定代表延伸的 Azure 資源管理員資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="c9e76-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="c9e76-115">Set-AzVMDscExtension Cmdlet 會將此名稱設定為 AzVMDscExtensionStatus，這是 **Get-AzVMDscExtensionStatus** 所使用的相同值。</span><span class="sxs-lookup"><span data-stu-id="c9e76-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtensionStatus**.</span></span>
<span data-ttu-id="c9e76-116">只有在您變更了 Set Cmdlet 中的預設名稱，或在資源管理器範本中使用不同的資源名稱時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="c9e76-116">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="c9e76-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9e76-117">-ResourceGroupName</span></span>
<span data-ttu-id="c9e76-118">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c9e76-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c9e76-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="c9e76-119">-VMName</span></span>
<span data-ttu-id="c9e76-120">指定此 Cmdlet 取得 DSC 延伸狀態的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="c9e76-120">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9e76-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9e76-121">CommonParameters</span></span>
<span data-ttu-id="c9e76-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c9e76-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9e76-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c9e76-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9e76-124">輸入</span><span class="sxs-lookup"><span data-stu-id="c9e76-124">INPUTS</span></span>

### <span data-ttu-id="c9e76-125">所有</span><span class="sxs-lookup"><span data-stu-id="c9e76-125">None</span></span>
<span data-ttu-id="c9e76-126">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="c9e76-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c9e76-127">輸出</span><span class="sxs-lookup"><span data-stu-id="c9e76-127">OUTPUTS</span></span>

### <span data-ttu-id="c9e76-128">PSVirtualMachineInstanceView 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="c9e76-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="c9e76-129">筆記</span><span class="sxs-lookup"><span data-stu-id="c9e76-129">NOTES</span></span>

## <span data-ttu-id="c9e76-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="c9e76-130">RELATED LINKS</span></span>

[<span data-ttu-id="c9e76-131">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="c9e76-131">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)



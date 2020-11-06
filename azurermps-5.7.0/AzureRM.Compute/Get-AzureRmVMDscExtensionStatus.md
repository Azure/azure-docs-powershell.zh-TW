---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
ms.openlocfilehash: 7cb7f175cc15e7d4e0915b6af9ef6fe6bdfc74d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446399"
---
# <span data-ttu-id="2de8e-101">Get-AzureRmVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="2de8e-101">Get-AzureRmVMDscExtensionStatus</span></span>

## <span data-ttu-id="2de8e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2de8e-102">SYNOPSIS</span></span>
<span data-ttu-id="2de8e-103">取得虛擬機器的 DSC 延伸處理常式狀態。</span><span class="sxs-lookup"><span data-stu-id="2de8e-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2de8e-104">句法</span><span class="sxs-lookup"><span data-stu-id="2de8e-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="2de8e-105">說明</span><span class="sxs-lookup"><span data-stu-id="2de8e-105">DESCRIPTION</span></span>
<span data-ttu-id="2de8e-106">AzureRmVMDscExtensionStatus Cmdlet 會針對資源群組中的虛擬機器， **取得** 所需狀態配置 (DSC) 延伸處理常式的狀態設定。</span><span class="sxs-lookup"><span data-stu-id="2de8e-106">The **Get-AzureRmVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="2de8e-107">套用配置時，此 Cmdlet 會產生與 Start-DscConfiguration Cmdlet 一致的輸出。</span><span class="sxs-lookup"><span data-stu-id="2de8e-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="2de8e-108">示例</span><span class="sxs-lookup"><span data-stu-id="2de8e-108">EXAMPLES</span></span>

## <span data-ttu-id="2de8e-109">參數</span><span class="sxs-lookup"><span data-stu-id="2de8e-109">PARAMETERS</span></span>

### <span data-ttu-id="2de8e-110">-名稱</span><span class="sxs-lookup"><span data-stu-id="2de8e-110">-Name</span></span>
<span data-ttu-id="2de8e-111">指定代表延伸的 Azure 資源管理員資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="2de8e-111">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="2de8e-112">Set-AzureRmVMDscExtension Cmdlet 會將此名稱設定為 AzureRmVMDscExtensionStatus，這是 **Get-AzureRmVMDscExtensionStatus** 所使用的相同值。</span><span class="sxs-lookup"><span data-stu-id="2de8e-112">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtensionStatus**.</span></span>
<span data-ttu-id="2de8e-113">只有在您變更了 Set Cmdlet 中的預設名稱，或在資源管理器範本中使用不同的資源名稱時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="2de8e-113">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="2de8e-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2de8e-114">-ResourceGroupName</span></span>
<span data-ttu-id="2de8e-115">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2de8e-115">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="2de8e-116">-VMName</span><span class="sxs-lookup"><span data-stu-id="2de8e-116">-VMName</span></span>
<span data-ttu-id="2de8e-117">指定此 Cmdlet 取得 DSC 延伸狀態的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="2de8e-117">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

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

### <span data-ttu-id="2de8e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2de8e-118">CommonParameters</span></span>
<span data-ttu-id="2de8e-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2de8e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2de8e-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2de8e-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2de8e-121">輸入</span><span class="sxs-lookup"><span data-stu-id="2de8e-121">INPUTS</span></span>

### <span data-ttu-id="2de8e-122">所有</span><span class="sxs-lookup"><span data-stu-id="2de8e-122">None</span></span>
<span data-ttu-id="2de8e-123">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="2de8e-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2de8e-124">輸出</span><span class="sxs-lookup"><span data-stu-id="2de8e-124">OUTPUTS</span></span>

## <span data-ttu-id="2de8e-125">筆記</span><span class="sxs-lookup"><span data-stu-id="2de8e-125">NOTES</span></span>

## <span data-ttu-id="2de8e-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="2de8e-126">RELATED LINKS</span></span>

[<span data-ttu-id="2de8e-127">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="2de8e-127">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)



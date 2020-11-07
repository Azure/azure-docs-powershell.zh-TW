---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdscextensionstatus
schema: 2.0.0
ms.openlocfilehash: b6ec9918657c191e31e10c04b799603654d39d56
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93799986"
---
# <span data-ttu-id="14383-101">Get-AzureRmVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="14383-101">Get-AzureRmVMDscExtensionStatus</span></span>

## <span data-ttu-id="14383-102">摘要</span><span class="sxs-lookup"><span data-stu-id="14383-102">SYNOPSIS</span></span>
<span data-ttu-id="14383-103">取得虛擬機器的 DSC 延伸處理常式狀態。</span><span class="sxs-lookup"><span data-stu-id="14383-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14383-104">句法</span><span class="sxs-lookup"><span data-stu-id="14383-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14383-105">說明</span><span class="sxs-lookup"><span data-stu-id="14383-105">DESCRIPTION</span></span>
<span data-ttu-id="14383-106">AzureRmVMDscExtensionStatus Cmdlet 會針對資源群組中的虛擬機器， **取得** 所需狀態配置 (DSC) 延伸處理常式的狀態設定。</span><span class="sxs-lookup"><span data-stu-id="14383-106">The **Get-AzureRmVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="14383-107">套用配置時，此 Cmdlet 會產生與 Start-DscConfiguration Cmdlet 一致的輸出。</span><span class="sxs-lookup"><span data-stu-id="14383-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="14383-108">示例</span><span class="sxs-lookup"><span data-stu-id="14383-108">EXAMPLES</span></span>

### <span data-ttu-id="14383-109">sr-1</span><span class="sxs-lookup"><span data-stu-id="14383-109">1:</span></span>
```

```

## <span data-ttu-id="14383-110">參數</span><span class="sxs-lookup"><span data-stu-id="14383-110">PARAMETERS</span></span>

### <span data-ttu-id="14383-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14383-111">-DefaultProfile</span></span>
<span data-ttu-id="14383-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="14383-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14383-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="14383-113">-Name</span></span>
<span data-ttu-id="14383-114">指定代表延伸的 Azure 資源管理員資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="14383-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="14383-115">Set-AzureRmVMDscExtension Cmdlet 會將此名稱設定為 AzureRmVMDscExtensionStatus，這是 **Get-AzureRmVMDscExtensionStatus** 所使用的相同值。</span><span class="sxs-lookup"><span data-stu-id="14383-115">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtensionStatus**.</span></span>
<span data-ttu-id="14383-116">只有在您變更了 Set Cmdlet 中的預設名稱，或在資源管理器範本中使用不同的資源名稱時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="14383-116">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="14383-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14383-117">-ResourceGroupName</span></span>
<span data-ttu-id="14383-118">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="14383-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="14383-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="14383-119">-VMName</span></span>
<span data-ttu-id="14383-120">指定此 Cmdlet 取得 DSC 延伸狀態的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="14383-120">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

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

### <span data-ttu-id="14383-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14383-121">CommonParameters</span></span>
<span data-ttu-id="14383-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="14383-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14383-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="14383-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14383-124">輸入</span><span class="sxs-lookup"><span data-stu-id="14383-124">INPUTS</span></span>

### <span data-ttu-id="14383-125">所有</span><span class="sxs-lookup"><span data-stu-id="14383-125">None</span></span>
<span data-ttu-id="14383-126">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="14383-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="14383-127">輸出</span><span class="sxs-lookup"><span data-stu-id="14383-127">OUTPUTS</span></span>

### <span data-ttu-id="14383-128">PSVirtualMachineInstanceView 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="14383-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="14383-129">筆記</span><span class="sxs-lookup"><span data-stu-id="14383-129">NOTES</span></span>

## <span data-ttu-id="14383-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="14383-130">RELATED LINKS</span></span>

[<span data-ttu-id="14383-131">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="14383-131">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)



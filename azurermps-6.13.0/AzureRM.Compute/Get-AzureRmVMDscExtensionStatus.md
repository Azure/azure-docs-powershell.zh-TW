---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdscextensionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMDscExtensionStatus.md
ms.openlocfilehash: 482d2d5b7dd88618bb29270f6ef3cec4e133e842
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624904"
---
# <span data-ttu-id="3fc45-101">Get-AzureRmVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="3fc45-101">Get-AzureRmVMDscExtensionStatus</span></span>

## <span data-ttu-id="3fc45-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3fc45-102">SYNOPSIS</span></span>
<span data-ttu-id="3fc45-103">取得虛擬機器的 DSC 延伸處理常式狀態。</span><span class="sxs-lookup"><span data-stu-id="3fc45-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fc45-104">句法</span><span class="sxs-lookup"><span data-stu-id="3fc45-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fc45-105">說明</span><span class="sxs-lookup"><span data-stu-id="3fc45-105">DESCRIPTION</span></span>
<span data-ttu-id="3fc45-106">AzureRmVMDscExtensionStatus Cmdlet 會針對資源群組中的虛擬機器， **取得** 所需狀態配置 (DSC) 延伸處理常式的狀態設定。</span><span class="sxs-lookup"><span data-stu-id="3fc45-106">The **Get-AzureRmVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="3fc45-107">套用配置時，此 Cmdlet 會產生與 Start-DscConfiguration Cmdlet 一致的輸出。</span><span class="sxs-lookup"><span data-stu-id="3fc45-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="3fc45-108">示例</span><span class="sxs-lookup"><span data-stu-id="3fc45-108">EXAMPLES</span></span>

## <span data-ttu-id="3fc45-109">參數</span><span class="sxs-lookup"><span data-stu-id="3fc45-109">PARAMETERS</span></span>

### <span data-ttu-id="3fc45-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fc45-110">-DefaultProfile</span></span>
<span data-ttu-id="3fc45-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3fc45-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fc45-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="3fc45-112">-Name</span></span>
<span data-ttu-id="3fc45-113">指定代表延伸的 Azure 資源管理員資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="3fc45-113">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="3fc45-114">Set-AzureRmVMDscExtension Cmdlet 會將此名稱設定為 AzureRmVMDscExtensionStatus，這是 **Get-AzureRmVMDscExtensionStatus** 所使用的相同值。</span><span class="sxs-lookup"><span data-stu-id="3fc45-114">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtensionStatus**.</span></span>
<span data-ttu-id="3fc45-115">只有在您變更了 Set Cmdlet 中的預設名稱，或在資源管理器範本中使用不同的資源名稱時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="3fc45-115">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="3fc45-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fc45-116">-ResourceGroupName</span></span>
<span data-ttu-id="3fc45-117">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3fc45-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3fc45-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="3fc45-118">-VMName</span></span>
<span data-ttu-id="3fc45-119">指定此 Cmdlet 取得 DSC 延伸狀態的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="3fc45-119">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fc45-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fc45-120">CommonParameters</span></span>
<span data-ttu-id="3fc45-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3fc45-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fc45-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3fc45-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fc45-123">輸入</span><span class="sxs-lookup"><span data-stu-id="3fc45-123">INPUTS</span></span>

### <span data-ttu-id="3fc45-124">System.object</span><span class="sxs-lookup"><span data-stu-id="3fc45-124">System.String</span></span>

## <span data-ttu-id="3fc45-125">輸出</span><span class="sxs-lookup"><span data-stu-id="3fc45-125">OUTPUTS</span></span>

### <span data-ttu-id="3fc45-126">PSVirtualMachineInstanceView 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="3fc45-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="3fc45-127">筆記</span><span class="sxs-lookup"><span data-stu-id="3fc45-127">NOTES</span></span>

## <span data-ttu-id="3fc45-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="3fc45-128">RELATED LINKS</span></span>

[<span data-ttu-id="3fc45-129">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="3fc45-129">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)



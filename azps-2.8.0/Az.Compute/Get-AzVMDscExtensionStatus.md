---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextensionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
ms.openlocfilehash: caf6f142c9669ba3f1b5f343c4bbb1a4dc978a97
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613377"
---
# <span data-ttu-id="a1482-101">Get-AzVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="a1482-101">Get-AzVMDscExtensionStatus</span></span>

## <span data-ttu-id="a1482-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a1482-102">SYNOPSIS</span></span>
<span data-ttu-id="a1482-103">取得虛擬機器的 DSC 延伸處理常式狀態。</span><span class="sxs-lookup"><span data-stu-id="a1482-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

## <span data-ttu-id="a1482-104">句法</span><span class="sxs-lookup"><span data-stu-id="a1482-104">SYNTAX</span></span>

```
Get-AzVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1482-105">說明</span><span class="sxs-lookup"><span data-stu-id="a1482-105">DESCRIPTION</span></span>
<span data-ttu-id="a1482-106">AzVMDscExtensionStatus Cmdlet 會針對資源群組中的虛擬機器， **取得** 所需狀態配置 (DSC) 延伸處理常式的狀態設定。</span><span class="sxs-lookup"><span data-stu-id="a1482-106">The **Get-AzVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="a1482-107">套用配置時，此 Cmdlet 會產生與 Start-DscConfiguration Cmdlet 一致的輸出。</span><span class="sxs-lookup"><span data-stu-id="a1482-107">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="a1482-108">示例</span><span class="sxs-lookup"><span data-stu-id="a1482-108">EXAMPLES</span></span>

## <span data-ttu-id="a1482-109">參數</span><span class="sxs-lookup"><span data-stu-id="a1482-109">PARAMETERS</span></span>

### <span data-ttu-id="a1482-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1482-110">-DefaultProfile</span></span>
<span data-ttu-id="a1482-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a1482-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1482-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="a1482-112">-Name</span></span>
<span data-ttu-id="a1482-113">指定代表延伸的 Azure 資源管理員資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1482-113">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="a1482-114">Set-AzVMDscExtension Cmdlet 會將此名稱設定為 AzVMDscExtensionStatus，這是 **Get-AzVMDscExtensionStatus** 所使用的相同值。</span><span class="sxs-lookup"><span data-stu-id="a1482-114">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtensionStatus**.</span></span>
<span data-ttu-id="a1482-115">只有在您變更了 Set Cmdlet 中的預設名稱，或在資源管理器範本中使用不同的資源名稱時，才能指定此參數。</span><span class="sxs-lookup"><span data-stu-id="a1482-115">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="a1482-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1482-116">-ResourceGroupName</span></span>
<span data-ttu-id="a1482-117">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1482-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a1482-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="a1482-118">-VMName</span></span>
<span data-ttu-id="a1482-119">指定此 Cmdlet 取得 DSC 延伸狀態的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="a1482-119">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

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

### <span data-ttu-id="a1482-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1482-120">CommonParameters</span></span>
<span data-ttu-id="a1482-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a1482-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1482-122">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a1482-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1482-123">輸入</span><span class="sxs-lookup"><span data-stu-id="a1482-123">INPUTS</span></span>

### <span data-ttu-id="a1482-124">System.object</span><span class="sxs-lookup"><span data-stu-id="a1482-124">System.String</span></span>

## <span data-ttu-id="a1482-125">輸出</span><span class="sxs-lookup"><span data-stu-id="a1482-125">OUTPUTS</span></span>

### <span data-ttu-id="a1482-126">PSVirtualMachineInstanceView 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="a1482-126">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="a1482-127">筆記</span><span class="sxs-lookup"><span data-stu-id="a1482-127">NOTES</span></span>

## <span data-ttu-id="a1482-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1482-128">RELATED LINKS</span></span>

[<span data-ttu-id="a1482-129">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="a1482-129">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)



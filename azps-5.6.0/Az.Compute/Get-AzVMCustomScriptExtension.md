---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
ms.openlocfilehash: 4e722e897b23ce1e7ea7c30a6caa393be75f893c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909181"
---
# <span data-ttu-id="44dc4-101">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="44dc4-101">Get-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="44dc4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="44dc4-102">SYNOPSIS</span></span>
<span data-ttu-id="44dc4-103">獲得自訂腳本擴充功能的資訊。</span><span class="sxs-lookup"><span data-stu-id="44dc4-103">Gets information about a custom script extension.</span></span>

## <span data-ttu-id="44dc4-104">語法</span><span class="sxs-lookup"><span data-stu-id="44dc4-104">SYNTAX</span></span>

```
Get-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44dc4-105">描述</span><span class="sxs-lookup"><span data-stu-id="44dc4-105">DESCRIPTION</span></span>
<span data-ttu-id="44dc4-106">**Get-AzTOMCustomScriptExtension** Cmdlet 會取得虛擬機器上自訂腳本虛擬機器擴充功能的資訊。</span><span class="sxs-lookup"><span data-stu-id="44dc4-106">The **Get-AzVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="44dc4-107">例子</span><span class="sxs-lookup"><span data-stu-id="44dc4-107">EXAMPLES</span></span>

### <span data-ttu-id="44dc4-108">範例 1：取得自訂腳本擴充功能</span><span class="sxs-lookup"><span data-stu-id="44dc4-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="44dc4-109">此命令會針對名為 VirtualMachine07 的虛擬機器，獲得名為 ContosoCustomScript 的自訂腳本副檔名。</span><span class="sxs-lookup"><span data-stu-id="44dc4-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="44dc4-110">範例 2：取得自訂腳本擴充功能的實例視圖</span><span class="sxs-lookup"><span data-stu-id="44dc4-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="44dc4-111">此命令會針對名為 VirtualMachine07 的虛擬機器，獲得名為 ContosoCustomScript 的自訂腳本副檔名的實例視圖。</span><span class="sxs-lookup"><span data-stu-id="44dc4-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="44dc4-112">參數</span><span class="sxs-lookup"><span data-stu-id="44dc4-112">PARAMETERS</span></span>

### <span data-ttu-id="44dc4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44dc4-113">-DefaultProfile</span></span>
<span data-ttu-id="44dc4-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="44dc4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44dc4-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="44dc4-115">-Name</span></span>
<span data-ttu-id="44dc4-116">指定此 Cmdlet 會獲得相關資訊的自訂腳本副檔名。</span><span class="sxs-lookup"><span data-stu-id="44dc4-116">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44dc4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44dc4-117">-ResourceGroupName</span></span>
<span data-ttu-id="44dc4-118">指定虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="44dc4-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="44dc4-119">-狀態</span><span class="sxs-lookup"><span data-stu-id="44dc4-119">-Status</span></span>
<span data-ttu-id="44dc4-120">表示此 Cmdlet 會獲得自訂腳本擴充功能的實例視圖。</span><span class="sxs-lookup"><span data-stu-id="44dc4-120">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44dc4-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="44dc4-121">-VMName</span></span>
<span data-ttu-id="44dc4-122">指定此 Cmdlet 會擴展為自訂腳本的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="44dc4-122">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44dc4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44dc4-123">CommonParameters</span></span>
<span data-ttu-id="44dc4-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="44dc4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44dc4-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44dc4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44dc4-126">輸入</span><span class="sxs-lookup"><span data-stu-id="44dc4-126">INPUTS</span></span>

### <span data-ttu-id="44dc4-127">System.String</span><span class="sxs-lookup"><span data-stu-id="44dc4-127">System.String</span></span>

### <span data-ttu-id="44dc4-128">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="44dc4-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="44dc4-129">輸出</span><span class="sxs-lookup"><span data-stu-id="44dc4-129">OUTPUTS</span></span>

### <span data-ttu-id="44dc4-130">Microsoft.Azure.Commands.Compute.models.VirtualMachineCustomScriptExtensionCoNtext</span><span class="sxs-lookup"><span data-stu-id="44dc4-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span></span>

## <span data-ttu-id="44dc4-131">筆記</span><span class="sxs-lookup"><span data-stu-id="44dc4-131">NOTES</span></span>

## <span data-ttu-id="44dc4-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="44dc4-132">RELATED LINKS</span></span>

[<span data-ttu-id="44dc4-133">Get-AzEVAccessExtension</span><span class="sxs-lookup"><span data-stu-id="44dc4-133">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="44dc4-134">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="44dc4-134">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="44dc4-135">Get-Az解說ExtensionImage</span><span class="sxs-lookup"><span data-stu-id="44dc4-135">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)



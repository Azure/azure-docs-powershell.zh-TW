---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
ms.openlocfilehash: 307dccf0d5bb137ba83a6acf3a9b5db0b4606f7d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917385"
---
# <span data-ttu-id="860d2-101">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="860d2-101">Get-AzVMDscExtension</span></span>

## <span data-ttu-id="860d2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="860d2-102">SYNOPSIS</span></span>
<span data-ttu-id="860d2-103">獲得特定虛擬機器上的 DSC 擴充功能設定。</span><span class="sxs-lookup"><span data-stu-id="860d2-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

## <span data-ttu-id="860d2-104">語法</span><span class="sxs-lookup"><span data-stu-id="860d2-104">SYNTAX</span></span>

### <span data-ttu-id="860d2-105">GetDscExtension (預設) </span><span class="sxs-lookup"><span data-stu-id="860d2-105">GetDscExtension (Default)</span></span>
```
Get-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="860d2-106">VMParameterSet</span><span class="sxs-lookup"><span data-stu-id="860d2-106">VMParameterSet</span></span>
```
Get-AzVMDscExtension [-Status] [-VM <PSVirtualMachine>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="860d2-107">描述</span><span class="sxs-lookup"><span data-stu-id="860d2-107">DESCRIPTION</span></span>
<span data-ttu-id="860d2-108">**Get-Az VIRTUALDscExtension** Cmdlet 會取得特定虛擬機器上 (DSC) 副檔名的設定。</span><span class="sxs-lookup"><span data-stu-id="860d2-108">The **Get-AzVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="860d2-109">例子</span><span class="sxs-lookup"><span data-stu-id="860d2-109">EXAMPLES</span></span>

### <span data-ttu-id="860d2-110">範例 1：取得 DSC 擴充功能設定</span><span class="sxs-lookup"><span data-stu-id="860d2-110">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="860d2-111">此命令在名為 VM07 的虛擬機器上，會獲得名為 DSC 的擴充功能設定。</span><span class="sxs-lookup"><span data-stu-id="860d2-111">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="860d2-112">參數</span><span class="sxs-lookup"><span data-stu-id="860d2-112">PARAMETERS</span></span>

### <span data-ttu-id="860d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="860d2-113">-DefaultProfile</span></span>
<span data-ttu-id="860d2-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="860d2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="860d2-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="860d2-115">-Name</span></span>
<span data-ttu-id="860d2-116">指定代表擴充功能之 Azure Resource Manager 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="860d2-116">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="860d2-117">Cmdlet Set-AzVMDscExtension將這個名稱設定為 Microsoft.Powershell.DSC，這是 **Get-AzCMDscExtension 所使用的相同值**。</span><span class="sxs-lookup"><span data-stu-id="860d2-117">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtension**.</span></span>
<span data-ttu-id="860d2-118">只有在您變更 **Set-AzCMDscExtension** Cmdlet 中的預設名稱，或在 Resource Manager 範本中使用不同的資源名稱時，才指定此參數。</span><span class="sxs-lookup"><span data-stu-id="860d2-118">Specify this parameter only if you changed the default name in the **Set-AzVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="860d2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="860d2-119">-ResourceGroupName</span></span>
<span data-ttu-id="860d2-120">指定虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="860d2-120">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="860d2-121">-狀態</span><span class="sxs-lookup"><span data-stu-id="860d2-121">-Status</span></span>
<span data-ttu-id="860d2-122">表示此 Cmdlet 會獲得 DSC 擴充功能的實例視圖。</span><span class="sxs-lookup"><span data-stu-id="860d2-122">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="860d2-123">-VM</span><span class="sxs-lookup"><span data-stu-id="860d2-123">-VM</span></span>
<span data-ttu-id="860d2-124">指定擴充功能所位於的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="860d2-124">Specifies the virtual machine object the extension is on.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="860d2-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="860d2-125">-VMName</span></span>
<span data-ttu-id="860d2-126">指定此 Cmdlet 獲得 DSC 副檔名的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="860d2-126">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="860d2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="860d2-127">CommonParameters</span></span>
<span data-ttu-id="860d2-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="860d2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="860d2-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="860d2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="860d2-130">輸入</span><span class="sxs-lookup"><span data-stu-id="860d2-130">INPUTS</span></span>

### <span data-ttu-id="860d2-131">System.String</span><span class="sxs-lookup"><span data-stu-id="860d2-131">System.String</span></span>

### <span data-ttu-id="860d2-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="860d2-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="860d2-133">輸出</span><span class="sxs-lookup"><span data-stu-id="860d2-133">OUTPUTS</span></span>

### <span data-ttu-id="860d2-134">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionCoNtext</span><span class="sxs-lookup"><span data-stu-id="860d2-134">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="860d2-135">筆記</span><span class="sxs-lookup"><span data-stu-id="860d2-135">NOTES</span></span>

## <span data-ttu-id="860d2-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="860d2-136">RELATED LINKS</span></span>

[<span data-ttu-id="860d2-137">Remove-AzMSDscExtension</span><span class="sxs-lookup"><span data-stu-id="860d2-137">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="860d2-138">Set-AzMSDscExtension</span><span class="sxs-lookup"><span data-stu-id="860d2-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)



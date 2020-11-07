---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtension.md
ms.openlocfilehash: ba4ac8d48c72ffac164e447777670c48f529f68f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958767"
---
# <span data-ttu-id="e8b1f-101">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e8b1f-101">Get-AzVMDscExtension</span></span>

## <span data-ttu-id="e8b1f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8b1f-102">SYNOPSIS</span></span>
<span data-ttu-id="e8b1f-103">取得特定虛擬機器上的 DSC 延伸設定。</span><span class="sxs-lookup"><span data-stu-id="e8b1f-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

## <span data-ttu-id="e8b1f-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8b1f-104">SYNTAX</span></span>

```
Get-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8b1f-105">說明</span><span class="sxs-lookup"><span data-stu-id="e8b1f-105">DESCRIPTION</span></span>
<span data-ttu-id="e8b1f-106">AzVMDscExtension Cmdlet 會針對特定虛擬機器上的 DSC) 延伸 (， **取得** 所需狀態設定的設定。</span><span class="sxs-lookup"><span data-stu-id="e8b1f-106">The **Get-AzVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="e8b1f-107">示例</span><span class="sxs-lookup"><span data-stu-id="e8b1f-107">EXAMPLES</span></span>

### <span data-ttu-id="e8b1f-108">範例1：取得 DSC 延伸設定</span><span class="sxs-lookup"><span data-stu-id="e8b1f-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="e8b1f-109">這個命令會取得名為 VM07 的虛擬機器上名為 DSC 的副檔名設定。</span><span class="sxs-lookup"><span data-stu-id="e8b1f-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="e8b1f-110">參數</span><span class="sxs-lookup"><span data-stu-id="e8b1f-110">PARAMETERS</span></span>

### <span data-ttu-id="e8b1f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8b1f-111">-DefaultProfile</span></span>
<span data-ttu-id="e8b1f-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8b1f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8b1f-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8b1f-113">-Name</span></span>
<span data-ttu-id="e8b1f-114">指定代表延伸的 Azure 資源管理員資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8b1f-114">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="e8b1f-115">Set-AzVMDscExtension Cmdlet 會將此名稱設定為 AzVMDscExtension，這是 **Get-AzVMDscExtension** 所使用的相同值。</span><span class="sxs-lookup"><span data-stu-id="e8b1f-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtension**.</span></span>
<span data-ttu-id="e8b1f-116">如果您在 **AzVMDscExtension** Cmdlet 中變更了預設名稱，或在資源管理器範本中使用不同的資源名稱，請指定此參數。</span><span class="sxs-lookup"><span data-stu-id="e8b1f-116">Specify this parameter only if you changed the default name in the **Set-AzVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="e8b1f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8b1f-117">-ResourceGroupName</span></span>
<span data-ttu-id="e8b1f-118">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8b1f-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e8b1f-119">-狀態</span><span class="sxs-lookup"><span data-stu-id="e8b1f-119">-Status</span></span>
<span data-ttu-id="e8b1f-120">表示此 Cmdlet 會取得 DSC 延伸的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="e8b1f-120">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

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

### <span data-ttu-id="e8b1f-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="e8b1f-121">-VMName</span></span>
<span data-ttu-id="e8b1f-122">指定此 Cmdlet 取得 DSC 副檔名之虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8b1f-122">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

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

### <span data-ttu-id="e8b1f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8b1f-123">CommonParameters</span></span>
<span data-ttu-id="e8b1f-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8b1f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8b1f-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e8b1f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8b1f-126">輸入</span><span class="sxs-lookup"><span data-stu-id="e8b1f-126">INPUTS</span></span>

### <span data-ttu-id="e8b1f-127">System.object</span><span class="sxs-lookup"><span data-stu-id="e8b1f-127">System.String</span></span>

### <span data-ttu-id="e8b1f-128">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="e8b1f-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e8b1f-129">輸出</span><span class="sxs-lookup"><span data-stu-id="e8b1f-129">OUTPUTS</span></span>

### <span data-ttu-id="e8b1f-130">[VirtualMachineDscExtensionCoNtext] 的計算副檔名</span><span class="sxs-lookup"><span data-stu-id="e8b1f-130">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="e8b1f-131">筆記</span><span class="sxs-lookup"><span data-stu-id="e8b1f-131">NOTES</span></span>

## <span data-ttu-id="e8b1f-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8b1f-132">RELATED LINKS</span></span>

[<span data-ttu-id="e8b1f-133">移除-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e8b1f-133">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="e8b1f-134">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e8b1f-134">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)



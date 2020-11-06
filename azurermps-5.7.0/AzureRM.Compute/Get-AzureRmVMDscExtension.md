---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5B7A1BE6-F5F5-4968-BE32-7743D0E25FE3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDscExtension.md
ms.openlocfilehash: 0a3c54331b557b6be279ab5ce3f9fafad62b158c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446404"
---
# <span data-ttu-id="f7b02-101">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="f7b02-101">Get-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="f7b02-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f7b02-102">SYNOPSIS</span></span>
<span data-ttu-id="f7b02-103">取得特定虛擬機器上的 DSC 延伸設定。</span><span class="sxs-lookup"><span data-stu-id="f7b02-103">Gets the settings of the DSC extension on a particular virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7b02-104">句法</span><span class="sxs-lookup"><span data-stu-id="f7b02-104">SYNTAX</span></span>

```
Get-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="f7b02-105">說明</span><span class="sxs-lookup"><span data-stu-id="f7b02-105">DESCRIPTION</span></span>
<span data-ttu-id="f7b02-106">AzureRmVMDscExtension Cmdlet 會針對特定虛擬機器上的 DSC) 延伸 (， **取得** 所需狀態設定的設定。</span><span class="sxs-lookup"><span data-stu-id="f7b02-106">The **Get-AzureRmVMDscExtension** cmdlet gets the settings of the Desired State Configuration (DSC) extension on a particular virtual machine.</span></span>

## <span data-ttu-id="f7b02-107">示例</span><span class="sxs-lookup"><span data-stu-id="f7b02-107">EXAMPLES</span></span>

### <span data-ttu-id="f7b02-108">範例1：取得 DSC 延伸設定</span><span class="sxs-lookup"><span data-stu-id="f7b02-108">Example 1: Get the settings of a DSC extension</span></span>
```
PS C:\> Get-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup002" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="f7b02-109">這個命令會取得名為 VM07 的虛擬機器上名為 DSC 的副檔名設定。</span><span class="sxs-lookup"><span data-stu-id="f7b02-109">This command gets the settings of extension named DSC on the virtual machine named VM07.</span></span>

## <span data-ttu-id="f7b02-110">參數</span><span class="sxs-lookup"><span data-stu-id="f7b02-110">PARAMETERS</span></span>

### <span data-ttu-id="f7b02-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="f7b02-111">-Name</span></span>
<span data-ttu-id="f7b02-112">指定代表延伸的 Azure 資源管理員資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7b02-112">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="f7b02-113">Set-AzureRmVMDscExtension Cmdlet 會將此名稱設定為 AzureRmVMDscExtension，這是 **Get-AzureRmVMDscExtension** 所使用的相同值。</span><span class="sxs-lookup"><span data-stu-id="f7b02-113">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzureRmVMDscExtension**.</span></span>
<span data-ttu-id="f7b02-114">如果您在 **AzureRmVMDscExtension** Cmdlet 中變更了預設名稱，或在資源管理器範本中使用不同的資源名稱，請指定此參數。</span><span class="sxs-lookup"><span data-stu-id="f7b02-114">Specify this parameter only if you changed the default name in the **Set-AzureRmVMDscExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="f7b02-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7b02-115">-ResourceGroupName</span></span>
<span data-ttu-id="f7b02-116">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7b02-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f7b02-117">-狀態</span><span class="sxs-lookup"><span data-stu-id="f7b02-117">-Status</span></span>
<span data-ttu-id="f7b02-118">表示此 Cmdlet 會取得 DSC 延伸的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="f7b02-118">Indicates that this cmdlet gets the instance view of the DSC extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7b02-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="f7b02-119">-VMName</span></span>
<span data-ttu-id="f7b02-120">指定此 Cmdlet 取得 DSC 副檔名之虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7b02-120">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension.</span></span>

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

### <span data-ttu-id="f7b02-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7b02-121">CommonParameters</span></span>
<span data-ttu-id="f7b02-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f7b02-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7b02-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f7b02-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7b02-124">輸入</span><span class="sxs-lookup"><span data-stu-id="f7b02-124">INPUTS</span></span>

### <span data-ttu-id="f7b02-125">所有</span><span class="sxs-lookup"><span data-stu-id="f7b02-125">None</span></span>
<span data-ttu-id="f7b02-126">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="f7b02-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f7b02-127">輸出</span><span class="sxs-lookup"><span data-stu-id="f7b02-127">OUTPUTS</span></span>

### <span data-ttu-id="f7b02-128">[VirtualMachineDscExtensionCoNtext] 的計算副檔名</span><span class="sxs-lookup"><span data-stu-id="f7b02-128">Microsoft.Azure.Commands.Compute.Extension.DSC.VirtualMachineDscExtensionContext</span></span>

## <span data-ttu-id="f7b02-129">筆記</span><span class="sxs-lookup"><span data-stu-id="f7b02-129">NOTES</span></span>

## <span data-ttu-id="f7b02-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7b02-130">RELATED LINKS</span></span>

[<span data-ttu-id="f7b02-131">移除-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="f7b02-131">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="f7b02-132">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="f7b02-132">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)



---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMExtension.md
ms.openlocfilehash: 82ab2f02d47b17342f71b09eebe826fc48c07b81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446396"
---
# <span data-ttu-id="8157e-101">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="8157e-101">Get-AzureRmVMExtension</span></span>

## <span data-ttu-id="8157e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8157e-102">SYNOPSIS</span></span>
<span data-ttu-id="8157e-103">取得在虛擬機器上安裝之虛擬機器延伸的屬性。</span><span class="sxs-lookup"><span data-stu-id="8157e-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8157e-104">句法</span><span class="sxs-lookup"><span data-stu-id="8157e-104">SYNTAX</span></span>

```
Get-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="8157e-105">說明</span><span class="sxs-lookup"><span data-stu-id="8157e-105">DESCRIPTION</span></span>
<span data-ttu-id="8157e-106">**AzureRmVMExtension** Cmdlet 會取得在虛擬機器上安裝的虛擬機器延伸的屬性。</span><span class="sxs-lookup"><span data-stu-id="8157e-106">The **Get-AzureRmVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="8157e-107">指定要取得屬性之延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="8157e-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="8157e-108">若只要取得延伸的 [實例] 視圖，請指定 Status 參數。</span><span class="sxs-lookup"><span data-stu-id="8157e-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="8157e-109">示例</span><span class="sxs-lookup"><span data-stu-id="8157e-109">EXAMPLES</span></span>

### <span data-ttu-id="8157e-110">範例1：取得延伸的屬性</span><span class="sxs-lookup"><span data-stu-id="8157e-110">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"
```

<span data-ttu-id="8157e-111">這個命令會取得「資源群組」 ResourceGroup11 中名為 VirtualMachine22 的虛擬機器上名為 CustomScriptExtension 的副檔名的屬性。</span><span class="sxs-lookup"><span data-stu-id="8157e-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="8157e-112">範例2：取得延伸的實例視圖</span><span class="sxs-lookup"><span data-stu-id="8157e-112">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status
```

<span data-ttu-id="8157e-113">這個命令會針對資源群組 ResourceGroup11 中名為 VirtualMachine22 的虛擬機器上名為 CustomScriptExtension 的副檔名取得實例視圖。</span><span class="sxs-lookup"><span data-stu-id="8157e-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="8157e-114">參數</span><span class="sxs-lookup"><span data-stu-id="8157e-114">PARAMETERS</span></span>

### <span data-ttu-id="8157e-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="8157e-115">-Name</span></span>
<span data-ttu-id="8157e-116">指定延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="8157e-116">Specifies the name of an extension.</span></span>
<span data-ttu-id="8157e-117">這個 Cmdlet 會取得此參數指定之副檔名的屬性。</span><span class="sxs-lookup"><span data-stu-id="8157e-117">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8157e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8157e-118">-ResourceGroupName</span></span>
<span data-ttu-id="8157e-119">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8157e-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8157e-120">-狀態</span><span class="sxs-lookup"><span data-stu-id="8157e-120">-Status</span></span>
<span data-ttu-id="8157e-121">表示此 Cmdlet 只會取得延伸的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="8157e-121">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8157e-122">-VMName</span><span class="sxs-lookup"><span data-stu-id="8157e-122">-VMName</span></span>
<span data-ttu-id="8157e-123">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="8157e-123">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="8157e-124">這個 Cmdlet 會從虛擬機器中取得此參數指定之延伸的屬性。</span><span class="sxs-lookup"><span data-stu-id="8157e-124">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8157e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8157e-125">CommonParameters</span></span>
<span data-ttu-id="8157e-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8157e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8157e-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8157e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8157e-128">輸入</span><span class="sxs-lookup"><span data-stu-id="8157e-128">INPUTS</span></span>

### <span data-ttu-id="8157e-129">所有</span><span class="sxs-lookup"><span data-stu-id="8157e-129">None</span></span>
<span data-ttu-id="8157e-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="8157e-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8157e-131">輸出</span><span class="sxs-lookup"><span data-stu-id="8157e-131">OUTPUTS</span></span>

## <span data-ttu-id="8157e-132">筆記</span><span class="sxs-lookup"><span data-stu-id="8157e-132">NOTES</span></span>

## <span data-ttu-id="8157e-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="8157e-133">RELATED LINKS</span></span>

[<span data-ttu-id="8157e-134">移除-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="8157e-134">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)

[<span data-ttu-id="8157e-135">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="8157e-135">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)



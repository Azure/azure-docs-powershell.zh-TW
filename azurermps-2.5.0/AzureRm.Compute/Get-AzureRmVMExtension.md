---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmextension
schema: 2.0.0
ms.openlocfilehash: ba6d3c19216c8198d4e8cb41fd7fd178cf272ee4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800541"
---
# <span data-ttu-id="6f5af-101">Get-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="6f5af-101">Get-AzureRmVMExtension</span></span>

## <span data-ttu-id="6f5af-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6f5af-102">SYNOPSIS</span></span>
<span data-ttu-id="6f5af-103">取得在虛擬機器上安裝之虛擬機器延伸的屬性。</span><span class="sxs-lookup"><span data-stu-id="6f5af-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f5af-104">句法</span><span class="sxs-lookup"><span data-stu-id="6f5af-104">SYNTAX</span></span>

```
Get-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f5af-105">說明</span><span class="sxs-lookup"><span data-stu-id="6f5af-105">DESCRIPTION</span></span>
<span data-ttu-id="6f5af-106">**AzureRmVMExtension** Cmdlet 會取得在虛擬機器上安裝的虛擬機器延伸的屬性。</span><span class="sxs-lookup"><span data-stu-id="6f5af-106">The **Get-AzureRmVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="6f5af-107">指定要取得屬性之延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f5af-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="6f5af-108">若只要取得延伸的 [實例] 視圖，請指定 Status 參數。</span><span class="sxs-lookup"><span data-stu-id="6f5af-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="6f5af-109">示例</span><span class="sxs-lookup"><span data-stu-id="6f5af-109">EXAMPLES</span></span>

### <span data-ttu-id="6f5af-110">範例1：取得延伸的屬性</span><span class="sxs-lookup"><span data-stu-id="6f5af-110">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"
```

<span data-ttu-id="6f5af-111">這個命令會取得「資源群組」 ResourceGroup11 中名為 VirtualMachine22 的虛擬機器上名為 CustomScriptExtension 的副檔名的屬性。</span><span class="sxs-lookup"><span data-stu-id="6f5af-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="6f5af-112">範例2：取得延伸的實例視圖</span><span class="sxs-lookup"><span data-stu-id="6f5af-112">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status
```

<span data-ttu-id="6f5af-113">這個命令會針對資源群組 ResourceGroup11 中名為 VirtualMachine22 的虛擬機器上名為 CustomScriptExtension 的副檔名取得實例視圖。</span><span class="sxs-lookup"><span data-stu-id="6f5af-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="6f5af-114">參數</span><span class="sxs-lookup"><span data-stu-id="6f5af-114">PARAMETERS</span></span>

### <span data-ttu-id="6f5af-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f5af-115">-DefaultProfile</span></span>
<span data-ttu-id="6f5af-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6f5af-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f5af-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="6f5af-117">-Name</span></span>
<span data-ttu-id="6f5af-118">指定延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f5af-118">Specifies the name of an extension.</span></span>
<span data-ttu-id="6f5af-119">這個 Cmdlet 會取得此參數指定之副檔名的屬性。</span><span class="sxs-lookup"><span data-stu-id="6f5af-119">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

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

### <span data-ttu-id="6f5af-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f5af-120">-ResourceGroupName</span></span>
<span data-ttu-id="6f5af-121">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f5af-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6f5af-122">-狀態</span><span class="sxs-lookup"><span data-stu-id="6f5af-122">-Status</span></span>
<span data-ttu-id="6f5af-123">表示此 Cmdlet 只會取得延伸的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="6f5af-123">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="6f5af-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="6f5af-124">-VMName</span></span>
<span data-ttu-id="6f5af-125">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f5af-125">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="6f5af-126">這個 Cmdlet 會從虛擬機器中取得此參數指定之延伸的屬性。</span><span class="sxs-lookup"><span data-stu-id="6f5af-126">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="6f5af-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f5af-127">CommonParameters</span></span>
<span data-ttu-id="6f5af-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6f5af-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f5af-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6f5af-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f5af-130">輸入</span><span class="sxs-lookup"><span data-stu-id="6f5af-130">INPUTS</span></span>

### <span data-ttu-id="6f5af-131">所有</span><span class="sxs-lookup"><span data-stu-id="6f5af-131">None</span></span>
<span data-ttu-id="6f5af-132">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="6f5af-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6f5af-133">輸出</span><span class="sxs-lookup"><span data-stu-id="6f5af-133">OUTPUTS</span></span>

### <span data-ttu-id="6f5af-134">PSVirtualMachineExtension 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="6f5af-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="6f5af-135">筆記</span><span class="sxs-lookup"><span data-stu-id="6f5af-135">NOTES</span></span>

## <span data-ttu-id="6f5af-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f5af-136">RELATED LINKS</span></span>

[<span data-ttu-id="6f5af-137">移除-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="6f5af-137">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)

[<span data-ttu-id="6f5af-138">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="6f5af-138">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)



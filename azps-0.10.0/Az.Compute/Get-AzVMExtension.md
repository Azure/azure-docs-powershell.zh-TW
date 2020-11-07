---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: a8ac31efd77d5b8ff5c07920bb14b44f80ac0955
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796253"
---
# <span data-ttu-id="4bd8f-101">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="4bd8f-101">Get-AzVMExtension</span></span>

## <span data-ttu-id="4bd8f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4bd8f-102">SYNOPSIS</span></span>
<span data-ttu-id="4bd8f-103">取得在虛擬機器上安裝之虛擬機器延伸的屬性。</span><span class="sxs-lookup"><span data-stu-id="4bd8f-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

## <span data-ttu-id="4bd8f-104">句法</span><span class="sxs-lookup"><span data-stu-id="4bd8f-104">SYNTAX</span></span>

```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bd8f-105">說明</span><span class="sxs-lookup"><span data-stu-id="4bd8f-105">DESCRIPTION</span></span>
<span data-ttu-id="4bd8f-106">**AzVMExtension** Cmdlet 會取得在虛擬機器上安裝的虛擬機器延伸的屬性。</span><span class="sxs-lookup"><span data-stu-id="4bd8f-106">The **Get-AzVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="4bd8f-107">指定要取得屬性之延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="4bd8f-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="4bd8f-108">若只要取得延伸的 [實例] 視圖，請指定 Status 參數。</span><span class="sxs-lookup"><span data-stu-id="4bd8f-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="4bd8f-109">示例</span><span class="sxs-lookup"><span data-stu-id="4bd8f-109">EXAMPLES</span></span>

### <span data-ttu-id="4bd8f-110">範例1：取得延伸的屬性</span><span class="sxs-lookup"><span data-stu-id="4bd8f-110">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"
```

<span data-ttu-id="4bd8f-111">這個命令會取得「資源群組」 ResourceGroup11 中名為 VirtualMachine22 的虛擬機器上名為 CustomScriptExtension 的副檔名的屬性。</span><span class="sxs-lookup"><span data-stu-id="4bd8f-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="4bd8f-112">範例2：取得延伸的實例視圖</span><span class="sxs-lookup"><span data-stu-id="4bd8f-112">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status
```

<span data-ttu-id="4bd8f-113">這個命令會針對資源群組 ResourceGroup11 中名為 VirtualMachine22 的虛擬機器上名為 CustomScriptExtension 的副檔名取得實例視圖。</span><span class="sxs-lookup"><span data-stu-id="4bd8f-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="4bd8f-114">參數</span><span class="sxs-lookup"><span data-stu-id="4bd8f-114">PARAMETERS</span></span>

### <span data-ttu-id="4bd8f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bd8f-115">-DefaultProfile</span></span>
<span data-ttu-id="4bd8f-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4bd8f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bd8f-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="4bd8f-117">-Name</span></span>
<span data-ttu-id="4bd8f-118">指定延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="4bd8f-118">Specifies the name of an extension.</span></span>
<span data-ttu-id="4bd8f-119">這個 Cmdlet 會取得此參數指定之副檔名的屬性。</span><span class="sxs-lookup"><span data-stu-id="4bd8f-119">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

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

### <span data-ttu-id="4bd8f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bd8f-120">-ResourceGroupName</span></span>
<span data-ttu-id="4bd8f-121">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4bd8f-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4bd8f-122">-狀態</span><span class="sxs-lookup"><span data-stu-id="4bd8f-122">-Status</span></span>
<span data-ttu-id="4bd8f-123">表示此 Cmdlet 只會取得延伸的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="4bd8f-123">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="4bd8f-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="4bd8f-124">-VMName</span></span>
<span data-ttu-id="4bd8f-125">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="4bd8f-125">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="4bd8f-126">這個 Cmdlet 會從虛擬機器中取得此參數指定之延伸的屬性。</span><span class="sxs-lookup"><span data-stu-id="4bd8f-126">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="4bd8f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bd8f-127">CommonParameters</span></span>
<span data-ttu-id="4bd8f-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4bd8f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bd8f-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4bd8f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bd8f-130">輸入</span><span class="sxs-lookup"><span data-stu-id="4bd8f-130">INPUTS</span></span>

### <span data-ttu-id="4bd8f-131">所有</span><span class="sxs-lookup"><span data-stu-id="4bd8f-131">None</span></span>
<span data-ttu-id="4bd8f-132">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="4bd8f-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4bd8f-133">輸出</span><span class="sxs-lookup"><span data-stu-id="4bd8f-133">OUTPUTS</span></span>

### <span data-ttu-id="4bd8f-134">PSVirtualMachineExtension 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="4bd8f-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="4bd8f-135">筆記</span><span class="sxs-lookup"><span data-stu-id="4bd8f-135">NOTES</span></span>

## <span data-ttu-id="4bd8f-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="4bd8f-136">RELATED LINKS</span></span>

[<span data-ttu-id="4bd8f-137">移除-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="4bd8f-137">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)

[<span data-ttu-id="4bd8f-138">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="4bd8f-138">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)



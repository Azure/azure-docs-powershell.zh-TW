---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
ms.openlocfilehash: 0639907999b3e84f5f609a3f0c6f1063204438ca
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796273"
---
# <span data-ttu-id="62603-101">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="62603-101">Get-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="62603-102">摘要</span><span class="sxs-lookup"><span data-stu-id="62603-102">SYNOPSIS</span></span>
<span data-ttu-id="62603-103">取得有關自訂腳本延伸的資訊。</span><span class="sxs-lookup"><span data-stu-id="62603-103">Gets information about a custom script extension.</span></span>

## <span data-ttu-id="62603-104">句法</span><span class="sxs-lookup"><span data-stu-id="62603-104">SYNTAX</span></span>

```
Get-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62603-105">說明</span><span class="sxs-lookup"><span data-stu-id="62603-105">DESCRIPTION</span></span>
<span data-ttu-id="62603-106">**AzVMCustomScriptExtension** Cmdlet 會取得有關虛擬機器上自訂腳本虛擬電腦延伸的資訊。</span><span class="sxs-lookup"><span data-stu-id="62603-106">The **Get-AzVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="62603-107">示例</span><span class="sxs-lookup"><span data-stu-id="62603-107">EXAMPLES</span></span>

### <span data-ttu-id="62603-108">範例1：取得自訂腳本延伸</span><span class="sxs-lookup"><span data-stu-id="62603-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="62603-109">這個命令會針對名為 VirtualMachine07 的虛擬機器，取得名為 ContosoCustomScript 的自訂腳本副檔名。</span><span class="sxs-lookup"><span data-stu-id="62603-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="62603-110">範例2：取得自訂腳本延伸的實例視圖</span><span class="sxs-lookup"><span data-stu-id="62603-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="62603-111">這個命令會針對名為 VirtualMachine07 的虛擬機器，取得名為 ContosoCustomScript 之自訂腳本副檔名的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="62603-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="62603-112">參數</span><span class="sxs-lookup"><span data-stu-id="62603-112">PARAMETERS</span></span>

### <span data-ttu-id="62603-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62603-113">-DefaultProfile</span></span>
<span data-ttu-id="62603-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="62603-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62603-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="62603-115">-Name</span></span>
<span data-ttu-id="62603-116">指定此 Cmdlet 取得資訊之自訂腳本副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="62603-116">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="62603-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62603-117">-ResourceGroupName</span></span>
<span data-ttu-id="62603-118">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="62603-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="62603-119">-狀態</span><span class="sxs-lookup"><span data-stu-id="62603-119">-Status</span></span>
<span data-ttu-id="62603-120">表示此 Cmdlet 會取得自訂腳本延伸的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="62603-120">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="62603-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="62603-121">-VMName</span></span>
<span data-ttu-id="62603-122">指定此 Cmdlet 取得自訂腳本副檔名的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="62603-122">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="62603-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62603-123">CommonParameters</span></span>
<span data-ttu-id="62603-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="62603-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62603-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="62603-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62603-126">輸入</span><span class="sxs-lookup"><span data-stu-id="62603-126">INPUTS</span></span>

### <span data-ttu-id="62603-127">所有</span><span class="sxs-lookup"><span data-stu-id="62603-127">None</span></span>
<span data-ttu-id="62603-128">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="62603-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="62603-129">輸出</span><span class="sxs-lookup"><span data-stu-id="62603-129">OUTPUTS</span></span>

### <span data-ttu-id="62603-130">VirtualMachineCustomScriptExtensionCoNtext 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="62603-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span></span>

## <span data-ttu-id="62603-131">筆記</span><span class="sxs-lookup"><span data-stu-id="62603-131">NOTES</span></span>

## <span data-ttu-id="62603-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="62603-132">RELATED LINKS</span></span>

[<span data-ttu-id="62603-133">AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="62603-133">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="62603-134">AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="62603-134">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="62603-135">AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="62603-135">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)



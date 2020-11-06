---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: d06e2ca5ed51b89b78999c1e146ca75805c8a674
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452552"
---
# <span data-ttu-id="0e116-101">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="0e116-101">Get-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="0e116-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0e116-102">SYNOPSIS</span></span>
<span data-ttu-id="0e116-103">取得有關自訂腳本延伸的資訊。</span><span class="sxs-lookup"><span data-stu-id="0e116-103">Gets information about a custom script extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e116-104">句法</span><span class="sxs-lookup"><span data-stu-id="0e116-104">SYNTAX</span></span>

```
Get-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e116-105">說明</span><span class="sxs-lookup"><span data-stu-id="0e116-105">DESCRIPTION</span></span>
<span data-ttu-id="0e116-106">**AzureRmVMCustomScriptExtension** Cmdlet 會取得有關虛擬機器上自訂腳本虛擬電腦延伸的資訊。</span><span class="sxs-lookup"><span data-stu-id="0e116-106">The **Get-AzureRmVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="0e116-107">示例</span><span class="sxs-lookup"><span data-stu-id="0e116-107">EXAMPLES</span></span>

### <span data-ttu-id="0e116-108">範例1：取得自訂腳本延伸</span><span class="sxs-lookup"><span data-stu-id="0e116-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="0e116-109">這個命令會針對名為 VirtualMachine07 的虛擬機器，取得名為 ContosoCustomScript 的自訂腳本副檔名。</span><span class="sxs-lookup"><span data-stu-id="0e116-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="0e116-110">範例2：取得自訂腳本延伸的實例視圖</span><span class="sxs-lookup"><span data-stu-id="0e116-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="0e116-111">這個命令會針對名為 VirtualMachine07 的虛擬機器，取得名為 ContosoCustomScript 之自訂腳本副檔名的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="0e116-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="0e116-112">參數</span><span class="sxs-lookup"><span data-stu-id="0e116-112">PARAMETERS</span></span>

### <span data-ttu-id="0e116-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e116-113">-DefaultProfile</span></span>
<span data-ttu-id="0e116-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0e116-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e116-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="0e116-115">-Name</span></span>
<span data-ttu-id="0e116-116">指定此 Cmdlet 取得資訊之自訂腳本副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e116-116">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="0e116-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e116-117">-ResourceGroupName</span></span>
<span data-ttu-id="0e116-118">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e116-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0e116-119">-狀態</span><span class="sxs-lookup"><span data-stu-id="0e116-119">-Status</span></span>
<span data-ttu-id="0e116-120">表示此 Cmdlet 會取得自訂腳本延伸的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="0e116-120">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="0e116-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="0e116-121">-VMName</span></span>
<span data-ttu-id="0e116-122">指定此 Cmdlet 取得自訂腳本副檔名的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="0e116-122">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="0e116-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e116-123">CommonParameters</span></span>
<span data-ttu-id="0e116-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0e116-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e116-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0e116-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e116-126">輸入</span><span class="sxs-lookup"><span data-stu-id="0e116-126">INPUTS</span></span>

## <span data-ttu-id="0e116-127">輸出</span><span class="sxs-lookup"><span data-stu-id="0e116-127">OUTPUTS</span></span>

## <span data-ttu-id="0e116-128">筆記</span><span class="sxs-lookup"><span data-stu-id="0e116-128">NOTES</span></span>

## <span data-ttu-id="0e116-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="0e116-129">RELATED LINKS</span></span>

[<span data-ttu-id="0e116-130">AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="0e116-130">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="0e116-131">AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="0e116-131">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="0e116-132">AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="0e116-132">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)



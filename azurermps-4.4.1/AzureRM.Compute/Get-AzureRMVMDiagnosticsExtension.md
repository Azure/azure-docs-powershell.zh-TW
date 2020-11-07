---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
ms.openlocfilehash: fd401aa80f65888bc0540bb7975263108e0f8637
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623727"
---
# <span data-ttu-id="a2ff2-101">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a2ff2-101">Get-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="a2ff2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a2ff2-102">SYNOPSIS</span></span>
<span data-ttu-id="a2ff2-103">取得虛擬機器上的診斷延伸設定。</span><span class="sxs-lookup"><span data-stu-id="a2ff2-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2ff2-104">句法</span><span class="sxs-lookup"><span data-stu-id="a2ff2-104">SYNTAX</span></span>

```
Get-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2ff2-105">說明</span><span class="sxs-lookup"><span data-stu-id="a2ff2-105">DESCRIPTION</span></span>
<span data-ttu-id="a2ff2-106">**AzureRmVMDiagnosticsExtension** Cmdlet 會取得虛擬機器上 Azure Diagnostics 延伸的設定。</span><span class="sxs-lookup"><span data-stu-id="a2ff2-106">The **Get-AzureRmVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="a2ff2-107">示例</span><span class="sxs-lookup"><span data-stu-id="a2ff2-107">EXAMPLES</span></span>

### <span data-ttu-id="a2ff2-108">範例1：取得套用至虛擬機器的診斷延伸</span><span class="sxs-lookup"><span data-stu-id="a2ff2-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="a2ff2-109">這個命令會取得已套用到名為 ContosoVM22 的虛擬機器的診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="a2ff2-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="a2ff2-110">參數</span><span class="sxs-lookup"><span data-stu-id="a2ff2-110">PARAMETERS</span></span>

### <span data-ttu-id="a2ff2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2ff2-111">-DefaultProfile</span></span>
<span data-ttu-id="a2ff2-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2ff2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2ff2-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="a2ff2-113">-Name</span></span>
<span data-ttu-id="a2ff2-114">指定此 Cmdlet 取得其設定的診斷延伸名稱。</span><span class="sxs-lookup"><span data-stu-id="a2ff2-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2ff2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2ff2-115">-ResourceGroupName</span></span>
<span data-ttu-id="a2ff2-116">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2ff2-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a2ff2-117">-狀態</span><span class="sxs-lookup"><span data-stu-id="a2ff2-117">-Status</span></span>
<span data-ttu-id="a2ff2-118">指示此 Cmdlet 使用 Status 值。</span><span class="sxs-lookup"><span data-stu-id="a2ff2-118">Indicates that this cmdlet uses the Status value.</span></span>

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

### <span data-ttu-id="a2ff2-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="a2ff2-119">-VMName</span></span>
<span data-ttu-id="a2ff2-120">指定此 Cmdlet 取得診斷延伸的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="a2ff2-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="a2ff2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2ff2-121">CommonParameters</span></span>
<span data-ttu-id="a2ff2-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a2ff2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2ff2-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a2ff2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2ff2-124">輸入</span><span class="sxs-lookup"><span data-stu-id="a2ff2-124">INPUTS</span></span>

## <span data-ttu-id="a2ff2-125">輸出</span><span class="sxs-lookup"><span data-stu-id="a2ff2-125">OUTPUTS</span></span>

## <span data-ttu-id="a2ff2-126">筆記</span><span class="sxs-lookup"><span data-stu-id="a2ff2-126">NOTES</span></span>

## <span data-ttu-id="a2ff2-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2ff2-127">RELATED LINKS</span></span>

[<span data-ttu-id="a2ff2-128">移除-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a2ff2-128">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="a2ff2-129">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="a2ff2-129">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)



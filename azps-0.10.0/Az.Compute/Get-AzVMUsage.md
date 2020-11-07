---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: 66a74ed2fa389c0dd39fa9fc86570ff8d68dc1dc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796206"
---
# <span data-ttu-id="b3edf-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="b3edf-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="b3edf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b3edf-102">SYNOPSIS</span></span>
<span data-ttu-id="b3edf-103">取得位置的虛擬機器核心計數使用量。</span><span class="sxs-lookup"><span data-stu-id="b3edf-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="b3edf-104">句法</span><span class="sxs-lookup"><span data-stu-id="b3edf-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3edf-105">說明</span><span class="sxs-lookup"><span data-stu-id="b3edf-105">DESCRIPTION</span></span>
<span data-ttu-id="b3edf-106">**AzVMUsage** Cmdlet 會取得位置的虛擬機器核心計數使用量。</span><span class="sxs-lookup"><span data-stu-id="b3edf-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="b3edf-107">示例</span><span class="sxs-lookup"><span data-stu-id="b3edf-107">EXAMPLES</span></span>

### <span data-ttu-id="b3edf-108">範例1：取得某個位置的核心計數使用量</span><span class="sxs-lookup"><span data-stu-id="b3edf-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="b3edf-109">這個命令會取得位置中央的虛擬機器核心計數使用量。</span><span class="sxs-lookup"><span data-stu-id="b3edf-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="b3edf-110">參數</span><span class="sxs-lookup"><span data-stu-id="b3edf-110">PARAMETERS</span></span>

### <span data-ttu-id="b3edf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3edf-111">-DefaultProfile</span></span>
<span data-ttu-id="b3edf-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b3edf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3edf-113">-位置</span><span class="sxs-lookup"><span data-stu-id="b3edf-113">-Location</span></span>
<span data-ttu-id="b3edf-114">指定此 Cmdlet 取得虛擬機器核心計數使用量的位置。</span><span class="sxs-lookup"><span data-stu-id="b3edf-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="b3edf-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3edf-115">CommonParameters</span></span>
<span data-ttu-id="b3edf-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b3edf-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3edf-117">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b3edf-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3edf-118">輸入</span><span class="sxs-lookup"><span data-stu-id="b3edf-118">INPUTS</span></span>

### <span data-ttu-id="b3edf-119">所有</span><span class="sxs-lookup"><span data-stu-id="b3edf-119">None</span></span>
<span data-ttu-id="b3edf-120">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="b3edf-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b3edf-121">輸出</span><span class="sxs-lookup"><span data-stu-id="b3edf-121">OUTPUTS</span></span>

### <span data-ttu-id="b3edf-122">PSUsage 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="b3edf-122">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="b3edf-123">筆記</span><span class="sxs-lookup"><span data-stu-id="b3edf-123">NOTES</span></span>

## <span data-ttu-id="b3edf-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3edf-124">RELATED LINKS</span></span>

[<span data-ttu-id="b3edf-125">AzVM</span><span class="sxs-lookup"><span data-stu-id="b3edf-125">Get-AzVM</span></span>](./Get-AzVM.md)



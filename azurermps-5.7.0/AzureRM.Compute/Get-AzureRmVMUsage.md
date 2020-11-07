---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
ms.openlocfilehash: 5d4f114ef93e0febf7c113f73b8007a9322be752
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625921"
---
# <span data-ttu-id="3ded9-101">Get-AzureRmVMUsage</span><span class="sxs-lookup"><span data-stu-id="3ded9-101">Get-AzureRmVMUsage</span></span>

## <span data-ttu-id="3ded9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3ded9-102">SYNOPSIS</span></span>
<span data-ttu-id="3ded9-103">取得位置的虛擬機器核心計數使用量。</span><span class="sxs-lookup"><span data-stu-id="3ded9-103">Gets the virtual machine core count usage for a location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ded9-104">句法</span><span class="sxs-lookup"><span data-stu-id="3ded9-104">SYNTAX</span></span>

```
Get-AzureRmVMUsage [-Location] <String> [<CommonParameters>]
```

## <span data-ttu-id="3ded9-105">說明</span><span class="sxs-lookup"><span data-stu-id="3ded9-105">DESCRIPTION</span></span>
<span data-ttu-id="3ded9-106">**AzureRmVMUsage** Cmdlet 會取得位置的虛擬機器核心計數使用量。</span><span class="sxs-lookup"><span data-stu-id="3ded9-106">The **Get-AzureRmVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="3ded9-107">示例</span><span class="sxs-lookup"><span data-stu-id="3ded9-107">EXAMPLES</span></span>

### <span data-ttu-id="3ded9-108">範例1：取得某個位置的核心計數使用量</span><span class="sxs-lookup"><span data-stu-id="3ded9-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

<span data-ttu-id="3ded9-109">這個命令會取得位置中央的虛擬機器核心計數使用量。</span><span class="sxs-lookup"><span data-stu-id="3ded9-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="3ded9-110">參數</span><span class="sxs-lookup"><span data-stu-id="3ded9-110">PARAMETERS</span></span>

### <span data-ttu-id="3ded9-111">-位置</span><span class="sxs-lookup"><span data-stu-id="3ded9-111">-Location</span></span>
<span data-ttu-id="3ded9-112">指定此 Cmdlet 取得虛擬機器核心計數使用量的位置。</span><span class="sxs-lookup"><span data-stu-id="3ded9-112">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="3ded9-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ded9-113">CommonParameters</span></span>
<span data-ttu-id="3ded9-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3ded9-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ded9-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3ded9-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ded9-116">輸入</span><span class="sxs-lookup"><span data-stu-id="3ded9-116">INPUTS</span></span>

### <span data-ttu-id="3ded9-117">所有</span><span class="sxs-lookup"><span data-stu-id="3ded9-117">None</span></span>
<span data-ttu-id="3ded9-118">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="3ded9-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3ded9-119">輸出</span><span class="sxs-lookup"><span data-stu-id="3ded9-119">OUTPUTS</span></span>

## <span data-ttu-id="3ded9-120">筆記</span><span class="sxs-lookup"><span data-stu-id="3ded9-120">NOTES</span></span>

## <span data-ttu-id="3ded9-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="3ded9-121">RELATED LINKS</span></span>

[<span data-ttu-id="3ded9-122">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="3ded9-122">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)



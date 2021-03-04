---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: ef13cdfc9a137790c0d9aa842a0ba31841baa99b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917354"
---
# <span data-ttu-id="40b0d-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="40b0d-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="40b0d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="40b0d-102">SYNOPSIS</span></span>
<span data-ttu-id="40b0d-103">獲得位置的虛擬機器核心計數使用量。</span><span class="sxs-lookup"><span data-stu-id="40b0d-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="40b0d-104">語法</span><span class="sxs-lookup"><span data-stu-id="40b0d-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40b0d-105">描述</span><span class="sxs-lookup"><span data-stu-id="40b0d-105">DESCRIPTION</span></span>
<span data-ttu-id="40b0d-106">**Get-Az VIRTUALUsage** Cmdlet 會取得位置的虛擬機器核心計數使用量。</span><span class="sxs-lookup"><span data-stu-id="40b0d-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="40b0d-107">例子</span><span class="sxs-lookup"><span data-stu-id="40b0d-107">EXAMPLES</span></span>

### <span data-ttu-id="40b0d-108">範例 1：取得位置的核心計數使用量</span><span class="sxs-lookup"><span data-stu-id="40b0d-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="40b0d-109">此命令會針對美國中央位置使用虛擬機器核心計數。</span><span class="sxs-lookup"><span data-stu-id="40b0d-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="40b0d-110">參數</span><span class="sxs-lookup"><span data-stu-id="40b0d-110">PARAMETERS</span></span>

### <span data-ttu-id="40b0d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40b0d-111">-DefaultProfile</span></span>
<span data-ttu-id="40b0d-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="40b0d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40b0d-113">-位置</span><span class="sxs-lookup"><span data-stu-id="40b0d-113">-Location</span></span>
<span data-ttu-id="40b0d-114">指定此 Cmdlet 可得到虛擬機器核心計數使用量的位置。</span><span class="sxs-lookup"><span data-stu-id="40b0d-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="40b0d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40b0d-115">CommonParameters</span></span>
<span data-ttu-id="40b0d-116">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="40b0d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40b0d-117">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40b0d-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40b0d-118">輸入</span><span class="sxs-lookup"><span data-stu-id="40b0d-118">INPUTS</span></span>

### <span data-ttu-id="40b0d-119">System.String</span><span class="sxs-lookup"><span data-stu-id="40b0d-119">System.String</span></span>

## <span data-ttu-id="40b0d-120">輸出</span><span class="sxs-lookup"><span data-stu-id="40b0d-120">OUTPUTS</span></span>

### <span data-ttu-id="40b0d-121">Microsoft.Azure.Commands.Compute.models.PSUsage</span><span class="sxs-lookup"><span data-stu-id="40b0d-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="40b0d-122">筆記</span><span class="sxs-lookup"><span data-stu-id="40b0d-122">NOTES</span></span>

## <span data-ttu-id="40b0d-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="40b0d-123">RELATED LINKS</span></span>

[<span data-ttu-id="40b0d-124">Get-AzMS</span><span class="sxs-lookup"><span data-stu-id="40b0d-124">Get-AzVM</span></span>](./Get-AzVM.md)



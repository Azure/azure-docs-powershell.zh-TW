---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: 0996b327a0253e5f20c693fb8a3f3229597c80e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622779"
---
# <span data-ttu-id="1b2dc-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="1b2dc-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="1b2dc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1b2dc-102">SYNOPSIS</span></span>
<span data-ttu-id="1b2dc-103">取得位置的虛擬機器核心計數使用量。</span><span class="sxs-lookup"><span data-stu-id="1b2dc-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="1b2dc-104">句法</span><span class="sxs-lookup"><span data-stu-id="1b2dc-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b2dc-105">說明</span><span class="sxs-lookup"><span data-stu-id="1b2dc-105">DESCRIPTION</span></span>
<span data-ttu-id="1b2dc-106">**AzVMUsage** Cmdlet 會取得位置的虛擬機器核心計數使用量。</span><span class="sxs-lookup"><span data-stu-id="1b2dc-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="1b2dc-107">示例</span><span class="sxs-lookup"><span data-stu-id="1b2dc-107">EXAMPLES</span></span>

### <span data-ttu-id="1b2dc-108">範例1：取得某個位置的核心計數使用量</span><span class="sxs-lookup"><span data-stu-id="1b2dc-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="1b2dc-109">這個命令會取得位置中央的虛擬機器核心計數使用量。</span><span class="sxs-lookup"><span data-stu-id="1b2dc-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="1b2dc-110">參數</span><span class="sxs-lookup"><span data-stu-id="1b2dc-110">PARAMETERS</span></span>

### <span data-ttu-id="1b2dc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b2dc-111">-DefaultProfile</span></span>
<span data-ttu-id="1b2dc-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b2dc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b2dc-113">-位置</span><span class="sxs-lookup"><span data-stu-id="1b2dc-113">-Location</span></span>
<span data-ttu-id="1b2dc-114">指定此 Cmdlet 取得虛擬機器核心計數使用量的位置。</span><span class="sxs-lookup"><span data-stu-id="1b2dc-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="1b2dc-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b2dc-115">CommonParameters</span></span>
<span data-ttu-id="1b2dc-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1b2dc-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b2dc-117">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1b2dc-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b2dc-118">輸入</span><span class="sxs-lookup"><span data-stu-id="1b2dc-118">INPUTS</span></span>

### <span data-ttu-id="1b2dc-119">System.object</span><span class="sxs-lookup"><span data-stu-id="1b2dc-119">System.String</span></span>

## <span data-ttu-id="1b2dc-120">輸出</span><span class="sxs-lookup"><span data-stu-id="1b2dc-120">OUTPUTS</span></span>

### <span data-ttu-id="1b2dc-121">PSUsage 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="1b2dc-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="1b2dc-122">筆記</span><span class="sxs-lookup"><span data-stu-id="1b2dc-122">NOTES</span></span>

## <span data-ttu-id="1b2dc-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b2dc-123">RELATED LINKS</span></span>

[<span data-ttu-id="1b2dc-124">AzVM</span><span class="sxs-lookup"><span data-stu-id="1b2dc-124">Get-AzVM</span></span>](./Get-AzVM.md)



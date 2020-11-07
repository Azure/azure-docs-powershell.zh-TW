---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmusage
schema: 2.0.0
ms.openlocfilehash: 210c66f91836b40c719d91907fc78bd907d0fe86
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802582"
---
# <span data-ttu-id="cac47-101">Get-AzureRmVMUsage</span><span class="sxs-lookup"><span data-stu-id="cac47-101">Get-AzureRmVMUsage</span></span>

## <span data-ttu-id="cac47-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cac47-102">SYNOPSIS</span></span>
<span data-ttu-id="cac47-103">取得位置的虛擬機器核心計數使用量。</span><span class="sxs-lookup"><span data-stu-id="cac47-103">Gets the virtual machine core count usage for a location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cac47-104">句法</span><span class="sxs-lookup"><span data-stu-id="cac47-104">SYNTAX</span></span>

```
Get-AzureRmVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cac47-105">說明</span><span class="sxs-lookup"><span data-stu-id="cac47-105">DESCRIPTION</span></span>
<span data-ttu-id="cac47-106">**AzureRmVMUsage** Cmdlet 會取得位置的虛擬機器核心計數使用量。</span><span class="sxs-lookup"><span data-stu-id="cac47-106">The **Get-AzureRmVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="cac47-107">示例</span><span class="sxs-lookup"><span data-stu-id="cac47-107">EXAMPLES</span></span>

### <span data-ttu-id="cac47-108">範例1：取得某個位置的核心計數使用量</span><span class="sxs-lookup"><span data-stu-id="cac47-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

<span data-ttu-id="cac47-109">這個命令會取得位置中央的虛擬機器核心計數使用量。</span><span class="sxs-lookup"><span data-stu-id="cac47-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="cac47-110">參數</span><span class="sxs-lookup"><span data-stu-id="cac47-110">PARAMETERS</span></span>

### <span data-ttu-id="cac47-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cac47-111">-DefaultProfile</span></span>
<span data-ttu-id="cac47-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cac47-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cac47-113">-位置</span><span class="sxs-lookup"><span data-stu-id="cac47-113">-Location</span></span>
<span data-ttu-id="cac47-114">指定此 Cmdlet 取得虛擬機器核心計數使用量的位置。</span><span class="sxs-lookup"><span data-stu-id="cac47-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="cac47-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cac47-115">CommonParameters</span></span>
<span data-ttu-id="cac47-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cac47-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cac47-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cac47-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cac47-118">輸入</span><span class="sxs-lookup"><span data-stu-id="cac47-118">INPUTS</span></span>

### <span data-ttu-id="cac47-119">所有</span><span class="sxs-lookup"><span data-stu-id="cac47-119">None</span></span>
<span data-ttu-id="cac47-120">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="cac47-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cac47-121">輸出</span><span class="sxs-lookup"><span data-stu-id="cac47-121">OUTPUTS</span></span>

### <span data-ttu-id="cac47-122">PSUsage 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="cac47-122">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="cac47-123">筆記</span><span class="sxs-lookup"><span data-stu-id="cac47-123">NOTES</span></span>

## <span data-ttu-id="cac47-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="cac47-124">RELATED LINKS</span></span>

[<span data-ttu-id="cac47-125">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cac47-125">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)



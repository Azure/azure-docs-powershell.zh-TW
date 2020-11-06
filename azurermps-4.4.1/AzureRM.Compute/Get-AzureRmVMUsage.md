---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
ms.openlocfilehash: af360334ab546685deadad45c2ea3f8954c226f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452535"
---
# <span data-ttu-id="61e7a-101">Get-AzureRmVMUsage</span><span class="sxs-lookup"><span data-stu-id="61e7a-101">Get-AzureRmVMUsage</span></span>

## <span data-ttu-id="61e7a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="61e7a-102">SYNOPSIS</span></span>
<span data-ttu-id="61e7a-103">取得位置的虛擬機器核心計數使用量。</span><span class="sxs-lookup"><span data-stu-id="61e7a-103">Gets the virtual machine core count usage for a location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61e7a-104">句法</span><span class="sxs-lookup"><span data-stu-id="61e7a-104">SYNTAX</span></span>

```
Get-AzureRmVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61e7a-105">說明</span><span class="sxs-lookup"><span data-stu-id="61e7a-105">DESCRIPTION</span></span>
<span data-ttu-id="61e7a-106">**AzureRmVMUsage** Cmdlet 會取得位置的虛擬機器核心計數使用量。</span><span class="sxs-lookup"><span data-stu-id="61e7a-106">The **Get-AzureRmVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="61e7a-107">示例</span><span class="sxs-lookup"><span data-stu-id="61e7a-107">EXAMPLES</span></span>

### <span data-ttu-id="61e7a-108">範例1：取得某個位置的核心計數使用量</span><span class="sxs-lookup"><span data-stu-id="61e7a-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

<span data-ttu-id="61e7a-109">這個命令會取得位置中央的虛擬機器核心計數使用量。</span><span class="sxs-lookup"><span data-stu-id="61e7a-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="61e7a-110">參數</span><span class="sxs-lookup"><span data-stu-id="61e7a-110">PARAMETERS</span></span>

### <span data-ttu-id="61e7a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61e7a-111">-DefaultProfile</span></span>
<span data-ttu-id="61e7a-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="61e7a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61e7a-113">-位置</span><span class="sxs-lookup"><span data-stu-id="61e7a-113">-Location</span></span>
<span data-ttu-id="61e7a-114">指定此 Cmdlet 取得虛擬機器核心計數使用量的位置。</span><span class="sxs-lookup"><span data-stu-id="61e7a-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="61e7a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61e7a-115">CommonParameters</span></span>
<span data-ttu-id="61e7a-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="61e7a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61e7a-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="61e7a-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61e7a-118">輸入</span><span class="sxs-lookup"><span data-stu-id="61e7a-118">INPUTS</span></span>

## <span data-ttu-id="61e7a-119">輸出</span><span class="sxs-lookup"><span data-stu-id="61e7a-119">OUTPUTS</span></span>

## <span data-ttu-id="61e7a-120">筆記</span><span class="sxs-lookup"><span data-stu-id="61e7a-120">NOTES</span></span>

## <span data-ttu-id="61e7a-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="61e7a-121">RELATED LINKS</span></span>

[<span data-ttu-id="61e7a-122">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="61e7a-122">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)



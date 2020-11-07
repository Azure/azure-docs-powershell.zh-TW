---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
ms.openlocfilehash: d1ae8cf3d0fd05acf4fa4897d362bd2cde70b346
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959015"
---
# <span data-ttu-id="e3f03-101">Get-AzServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="e3f03-101">Get-AzServiceBusOperation</span></span>

## <span data-ttu-id="e3f03-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3f03-102">SYNOPSIS</span></span>
<span data-ttu-id="e3f03-103">清單支援的未列作業</span><span class="sxs-lookup"><span data-stu-id="e3f03-103">List supported ServiceBus Operations</span></span>

## <span data-ttu-id="e3f03-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3f03-104">SYNTAX</span></span>

```
Get-AzServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3f03-105">說明</span><span class="sxs-lookup"><span data-stu-id="e3f03-105">DESCRIPTION</span></span>
<span data-ttu-id="e3f03-106">**AzServiceBusOperation** Cmdlet 會列出未獲支援的作業。</span><span class="sxs-lookup"><span data-stu-id="e3f03-106">The **Get-AzServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="e3f03-107">示例</span><span class="sxs-lookup"><span data-stu-id="e3f03-107">EXAMPLES</span></span>

### <span data-ttu-id="e3f03-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e3f03-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusOperation
```

<span data-ttu-id="e3f03-109">列出未受支援的作業</span><span class="sxs-lookup"><span data-stu-id="e3f03-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="e3f03-110">參數</span><span class="sxs-lookup"><span data-stu-id="e3f03-110">PARAMETERS</span></span>

### <span data-ttu-id="e3f03-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3f03-111">-DefaultProfile</span></span>
<span data-ttu-id="e3f03-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3f03-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3f03-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3f03-113">CommonParameters</span></span>
<span data-ttu-id="e3f03-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3f03-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3f03-115">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e3f03-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3f03-116">輸入</span><span class="sxs-lookup"><span data-stu-id="e3f03-116">INPUTS</span></span>

### <span data-ttu-id="e3f03-117">所有</span><span class="sxs-lookup"><span data-stu-id="e3f03-117">None</span></span>

## <span data-ttu-id="e3f03-118">輸出</span><span class="sxs-lookup"><span data-stu-id="e3f03-118">OUTPUTS</span></span>

### <span data-ttu-id="e3f03-119">PSOperationAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e3f03-119">Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="e3f03-120">筆記</span><span class="sxs-lookup"><span data-stu-id="e3f03-120">NOTES</span></span>

## <span data-ttu-id="e3f03-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3f03-121">RELATED LINKS</span></span>

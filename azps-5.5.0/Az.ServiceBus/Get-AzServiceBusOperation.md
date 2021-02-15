---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
ms.openlocfilehash: d1ae8cf3d0fd05acf4fa4897d362bd2cde70b346
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142523"
---
# <span data-ttu-id="a76c7-101">Get-AzServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="a76c7-101">Get-AzServiceBusOperation</span></span>

## <span data-ttu-id="a76c7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a76c7-102">SYNOPSIS</span></span>
<span data-ttu-id="a76c7-103">清單支援的未列作業</span><span class="sxs-lookup"><span data-stu-id="a76c7-103">List supported ServiceBus Operations</span></span>

## <span data-ttu-id="a76c7-104">句法</span><span class="sxs-lookup"><span data-stu-id="a76c7-104">SYNTAX</span></span>

```
Get-AzServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a76c7-105">說明</span><span class="sxs-lookup"><span data-stu-id="a76c7-105">DESCRIPTION</span></span>
<span data-ttu-id="a76c7-106">**AzServiceBusOperation** Cmdlet 會列出未獲支援的作業。</span><span class="sxs-lookup"><span data-stu-id="a76c7-106">The **Get-AzServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="a76c7-107">示例</span><span class="sxs-lookup"><span data-stu-id="a76c7-107">EXAMPLES</span></span>

### <span data-ttu-id="a76c7-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a76c7-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusOperation
```

<span data-ttu-id="a76c7-109">列出未受支援的作業</span><span class="sxs-lookup"><span data-stu-id="a76c7-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="a76c7-110">參數</span><span class="sxs-lookup"><span data-stu-id="a76c7-110">PARAMETERS</span></span>

### <span data-ttu-id="a76c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a76c7-111">-DefaultProfile</span></span>
<span data-ttu-id="a76c7-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a76c7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a76c7-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a76c7-113">CommonParameters</span></span>
<span data-ttu-id="a76c7-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a76c7-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a76c7-115">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a76c7-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a76c7-116">輸入</span><span class="sxs-lookup"><span data-stu-id="a76c7-116">INPUTS</span></span>

### <span data-ttu-id="a76c7-117">所有</span><span class="sxs-lookup"><span data-stu-id="a76c7-117">None</span></span>

## <span data-ttu-id="a76c7-118">輸出</span><span class="sxs-lookup"><span data-stu-id="a76c7-118">OUTPUTS</span></span>

### <span data-ttu-id="a76c7-119">PSOperationAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a76c7-119">Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="a76c7-120">筆記</span><span class="sxs-lookup"><span data-stu-id="a76c7-120">NOTES</span></span>

## <span data-ttu-id="a76c7-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="a76c7-121">RELATED LINKS</span></span>

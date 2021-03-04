---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementsubscriptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscriptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscriptionKey.md
ms.openlocfilehash: 808a9f8d5ee4b15885e06e2ab4ac1fc7c5d1bed9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915689"
---
# <span data-ttu-id="89207-101">Get-AzApiManagementSubscriptionKey</span><span class="sxs-lookup"><span data-stu-id="89207-101">Get-AzApiManagementSubscriptionKey</span></span>

## <span data-ttu-id="89207-102">簡介</span><span class="sxs-lookup"><span data-stu-id="89207-102">SYNOPSIS</span></span>
<span data-ttu-id="89207-103">獲得訂閱金鑰。</span><span class="sxs-lookup"><span data-stu-id="89207-103">Gets subscription keys.</span></span>

## <span data-ttu-id="89207-104">語法</span><span class="sxs-lookup"><span data-stu-id="89207-104">SYNTAX</span></span>

```
Get-AzApiManagementSubscriptionKey -Context <PsApiManagementContext> -SubscriptionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89207-105">描述</span><span class="sxs-lookup"><span data-stu-id="89207-105">DESCRIPTION</span></span>
<span data-ttu-id="89207-106">**Get-AzApiManagementSubscriptionKey** Cmdlet 會取得指定訂閱的金鑰。</span><span class="sxs-lookup"><span data-stu-id="89207-106">The **Get-AzApiManagementSubscriptionKey** cmdlet gets a keys of a specified subscription.</span></span>

## <span data-ttu-id="89207-107">例子</span><span class="sxs-lookup"><span data-stu-id="89207-107">EXAMPLES</span></span>

### <span data-ttu-id="89207-108">範例 1：取得具有指定識別碼的訂閱金鑰</span><span class="sxs-lookup"><span data-stu-id="89207-108">Example 1: Get a subscription keys with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscriptionKey -Context $apimContext -SubscriptionId "0123456789"

PrimaryKey        : 5e48532634114fe999a6979ce0d63a64
SecondaryKey      : 0a8efaf85a664aa0a412241015c7c8f6
```

<span data-ttu-id="89207-109">此命令會按識別碼獲得訂閱。</span><span class="sxs-lookup"><span data-stu-id="89207-109">This command gets a subscription by ID.</span></span>

## <span data-ttu-id="89207-110">參數</span><span class="sxs-lookup"><span data-stu-id="89207-110">PARAMETERS</span></span>

### <span data-ttu-id="89207-111">-內容</span><span class="sxs-lookup"><span data-stu-id="89207-111">-Context</span></span>
<span data-ttu-id="89207-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="89207-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89207-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89207-113">-DefaultProfile</span></span>
<span data-ttu-id="89207-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="89207-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89207-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="89207-115">-SubscriptionId</span></span>
<span data-ttu-id="89207-116">指定訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="89207-116">Specifies a subscription identifier.</span></span>
<span data-ttu-id="89207-117">如果指定，此 Cmdlet 會根據識別碼尋找訂閱。</span><span class="sxs-lookup"><span data-stu-id="89207-117">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89207-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89207-118">CommonParameters</span></span>
<span data-ttu-id="89207-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="89207-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89207-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89207-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89207-121">輸入</span><span class="sxs-lookup"><span data-stu-id="89207-121">INPUTS</span></span>

### <span data-ttu-id="89207-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="89207-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="89207-123">System.String</span><span class="sxs-lookup"><span data-stu-id="89207-123">System.String</span></span>

## <span data-ttu-id="89207-124">輸出</span><span class="sxs-lookup"><span data-stu-id="89207-124">OUTPUTS</span></span>

### <span data-ttu-id="89207-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementSubscriptionKey</span><span class="sxs-lookup"><span data-stu-id="89207-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionKey</span></span>

## <span data-ttu-id="89207-126">筆記</span><span class="sxs-lookup"><span data-stu-id="89207-126">NOTES</span></span>

## <span data-ttu-id="89207-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="89207-127">RELATED LINKS</span></span>

[<span data-ttu-id="89207-128">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="89207-128">New-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="89207-129">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="89207-129">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="89207-130">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="89207-130">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="89207-131">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="89207-131">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)



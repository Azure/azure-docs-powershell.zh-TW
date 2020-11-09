---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscriptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscriptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscriptionKey.md
ms.openlocfilehash: 74362c511abde8baed24f1b484a916a9e9851426
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286692"
---
# <span data-ttu-id="f4b3a-101">Get-AzApiManagementSubscriptionKey</span><span class="sxs-lookup"><span data-stu-id="f4b3a-101">Get-AzApiManagementSubscriptionKey</span></span>

## <span data-ttu-id="f4b3a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f4b3a-102">SYNOPSIS</span></span>
<span data-ttu-id="f4b3a-103">取得訂閱金鑰。</span><span class="sxs-lookup"><span data-stu-id="f4b3a-103">Gets subscription keys.</span></span>

## <span data-ttu-id="f4b3a-104">句法</span><span class="sxs-lookup"><span data-stu-id="f4b3a-104">SYNTAX</span></span>

```
Get-AzApiManagementSubscriptionKey -Context <PsApiManagementContext> -SubscriptionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4b3a-105">說明</span><span class="sxs-lookup"><span data-stu-id="f4b3a-105">DESCRIPTION</span></span>
<span data-ttu-id="f4b3a-106">**AzApiManagementSubscriptionKey** Cmdlet 會取得指定訂閱的金鑰。</span><span class="sxs-lookup"><span data-stu-id="f4b3a-106">The **Get-AzApiManagementSubscriptionKey** cmdlet gets a keys of a specified subscription.</span></span>

## <span data-ttu-id="f4b3a-107">示例</span><span class="sxs-lookup"><span data-stu-id="f4b3a-107">EXAMPLES</span></span>

### <span data-ttu-id="f4b3a-108">範例1：取得具有指定識別碼的訂閱金鑰</span><span class="sxs-lookup"><span data-stu-id="f4b3a-108">Example 1: Get a subscription keys with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscriptionKey -Context $apimContext -SubscriptionId "0123456789"

PrimaryKey        : 5e48532634114fe999a6979ce0d63a64
SecondaryKey      : 0a8efaf85a664aa0a412241015c7c8f6
```

<span data-ttu-id="f4b3a-109">這個命令透過識別碼取得訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4b3a-109">This command gets a subscription by ID.</span></span>

## <span data-ttu-id="f4b3a-110">參數</span><span class="sxs-lookup"><span data-stu-id="f4b3a-110">PARAMETERS</span></span>

### <span data-ttu-id="f4b3a-111">-內容</span><span class="sxs-lookup"><span data-stu-id="f4b3a-111">-Context</span></span>
<span data-ttu-id="f4b3a-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="f4b3a-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f4b3a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4b3a-113">-DefaultProfile</span></span>
<span data-ttu-id="f4b3a-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4b3a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4b3a-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f4b3a-115">-SubscriptionId</span></span>
<span data-ttu-id="f4b3a-116">指定訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="f4b3a-116">Specifies a subscription identifier.</span></span>
<span data-ttu-id="f4b3a-117">如果已指定，此 Cmdlet 會依識別碼尋找訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4b3a-117">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="f4b3a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4b3a-118">CommonParameters</span></span>
<span data-ttu-id="f4b3a-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f4b3a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4b3a-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f4b3a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4b3a-121">輸入</span><span class="sxs-lookup"><span data-stu-id="f4b3a-121">INPUTS</span></span>

### <span data-ttu-id="f4b3a-122">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="f4b3a-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f4b3a-123">System.object</span><span class="sxs-lookup"><span data-stu-id="f4b3a-123">System.String</span></span>

## <span data-ttu-id="f4b3a-124">輸出</span><span class="sxs-lookup"><span data-stu-id="f4b3a-124">OUTPUTS</span></span>

### <span data-ttu-id="f4b3a-125">ServiceManagement. PsApiManagementSubscriptionKey （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="f4b3a-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionKey</span></span>

## <span data-ttu-id="f4b3a-126">筆記</span><span class="sxs-lookup"><span data-stu-id="f4b3a-126">NOTES</span></span>

## <span data-ttu-id="f4b3a-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4b3a-127">RELATED LINKS</span></span>

[<span data-ttu-id="f4b3a-128">新-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f4b3a-128">New-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="f4b3a-129">新-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f4b3a-129">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="f4b3a-130">移除-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f4b3a-130">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="f4b3a-131">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="f4b3a-131">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)



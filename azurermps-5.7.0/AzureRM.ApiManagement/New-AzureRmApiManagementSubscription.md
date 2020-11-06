---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 08685a84817f55e030a62b0b98ddc35be9f05843
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449425"
---
# <span data-ttu-id="0adb9-101">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0adb9-101">New-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="0adb9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0adb9-102">SYNOPSIS</span></span>
<span data-ttu-id="0adb9-103">建立訂閱。</span><span class="sxs-lookup"><span data-stu-id="0adb9-103">Creates a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0adb9-104">句法</span><span class="sxs-lookup"><span data-stu-id="0adb9-104">SYNTAX</span></span>

```
New-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 -Name <String> -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0adb9-105">說明</span><span class="sxs-lookup"><span data-stu-id="0adb9-105">DESCRIPTION</span></span>
<span data-ttu-id="0adb9-106">**新的-AzureRmApiManagementSubscription** Cmdlet 會建立訂閱。</span><span class="sxs-lookup"><span data-stu-id="0adb9-106">The **New-AzureRmApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="0adb9-107">示例</span><span class="sxs-lookup"><span data-stu-id="0adb9-107">EXAMPLES</span></span>

### <span data-ttu-id="0adb9-108">範例1：為使用者訂閱產品</span><span class="sxs-lookup"><span data-stu-id="0adb9-108">Example 1: Subscribe a user to a product</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="0adb9-109">這個命令會將現有的使用者訂閱至產品。</span><span class="sxs-lookup"><span data-stu-id="0adb9-109">This command subscribes an existing user to a product.</span></span>

## <span data-ttu-id="0adb9-110">參數</span><span class="sxs-lookup"><span data-stu-id="0adb9-110">PARAMETERS</span></span>

### <span data-ttu-id="0adb9-111">-內容</span><span class="sxs-lookup"><span data-stu-id="0adb9-111">-Context</span></span>
<span data-ttu-id="0adb9-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="0adb9-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0adb9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0adb9-113">-DefaultProfile</span></span>
<span data-ttu-id="0adb9-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0adb9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="0adb9-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="0adb9-115">-Name</span></span>
<span data-ttu-id="0adb9-116">指定訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="0adb9-116">Specifies the subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0adb9-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="0adb9-117">-PrimaryKey</span></span>
<span data-ttu-id="0adb9-118">指定訂閱主鍵。</span><span class="sxs-lookup"><span data-stu-id="0adb9-118">Specifies the subscription primary key.</span></span>
<span data-ttu-id="0adb9-119">如果未指定此參數，則會自動產生金鑰。</span><span class="sxs-lookup"><span data-stu-id="0adb9-119">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="0adb9-120">這個參數必須是1到300個字元長。</span><span class="sxs-lookup"><span data-stu-id="0adb9-120">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0adb9-121">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="0adb9-121">-ProductId</span></span>
<span data-ttu-id="0adb9-122">指定要訂閱的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="0adb9-122">Specifies the ID of the product to which to subscribe.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0adb9-123">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="0adb9-123">-SecondaryKey</span></span>
<span data-ttu-id="0adb9-124">指定訂閱次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="0adb9-124">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="0adb9-125">如果沒有指定，則會自動產生此參數。</span><span class="sxs-lookup"><span data-stu-id="0adb9-125">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="0adb9-126">這個參數必須是1到300個字元長。</span><span class="sxs-lookup"><span data-stu-id="0adb9-126">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0adb9-127">-State</span><span class="sxs-lookup"><span data-stu-id="0adb9-127">-State</span></span>
<span data-ttu-id="0adb9-128">指定訂閱狀態。</span><span class="sxs-lookup"><span data-stu-id="0adb9-128">Specifies the subscription state.</span></span>
<span data-ttu-id="0adb9-129">預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="0adb9-129">The default value is $Null.</span></span>

```yaml
Type: PsApiManagementSubscriptionState
Parameter Sets: (All)
Aliases: 
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0adb9-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0adb9-130">-SubscriptionId</span></span>
<span data-ttu-id="0adb9-131">指定訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="0adb9-131">Specifies the subscription ID.</span></span>
<span data-ttu-id="0adb9-132">如果沒有指定，則會產生此參數。</span><span class="sxs-lookup"><span data-stu-id="0adb9-132">This parameter is generated if not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0adb9-133">-UserId</span><span class="sxs-lookup"><span data-stu-id="0adb9-133">-UserId</span></span>
<span data-ttu-id="0adb9-134">指定訂閱者 ID。</span><span class="sxs-lookup"><span data-stu-id="0adb9-134">Specifies the subscriber ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0adb9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0adb9-135">CommonParameters</span></span>
<span data-ttu-id="0adb9-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0adb9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0adb9-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0adb9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0adb9-138">輸入</span><span class="sxs-lookup"><span data-stu-id="0adb9-138">INPUTS</span></span>

### <span data-ttu-id="0adb9-139">所有</span><span class="sxs-lookup"><span data-stu-id="0adb9-139">None</span></span>
<span data-ttu-id="0adb9-140">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="0adb9-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0adb9-141">輸出</span><span class="sxs-lookup"><span data-stu-id="0adb9-141">OUTPUTS</span></span>

### <span data-ttu-id="0adb9-142">ServiceManagement. PsApiManagementSubscription （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="0adb9-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="0adb9-143">筆記</span><span class="sxs-lookup"><span data-stu-id="0adb9-143">NOTES</span></span>

## <span data-ttu-id="0adb9-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="0adb9-144">RELATED LINKS</span></span>

[<span data-ttu-id="0adb9-145">AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0adb9-145">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="0adb9-146">移除-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0adb9-146">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="0adb9-147">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0adb9-147">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)



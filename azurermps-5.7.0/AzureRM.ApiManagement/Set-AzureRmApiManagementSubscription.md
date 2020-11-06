---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 62c1bd394dd509b81a8ea748c26c0465718926c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454775"
---
# <span data-ttu-id="c80ae-101">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c80ae-101">Set-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="c80ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c80ae-102">SYNOPSIS</span></span>
<span data-ttu-id="c80ae-103">設定現有的訂閱詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c80ae-103">Sets existing subscription details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c80ae-104">句法</span><span class="sxs-lookup"><span data-stu-id="c80ae-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c80ae-105">說明</span><span class="sxs-lookup"><span data-stu-id="c80ae-105">DESCRIPTION</span></span>
<span data-ttu-id="c80ae-106">**AzureRmApiManagementSubscription** Cmdlet 會設定現有的訂閱詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c80ae-106">The **Set-AzureRmApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="c80ae-107">示例</span><span class="sxs-lookup"><span data-stu-id="c80ae-107">EXAMPLES</span></span>

### <span data-ttu-id="c80ae-108">範例1：設定訂閱的狀態與主要和次要金鑰</span><span class="sxs-lookup"><span data-stu-id="c80ae-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="c80ae-109">這個命令會設定訂閱的主要和次要金鑰，並啟用。</span><span class="sxs-lookup"><span data-stu-id="c80ae-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="c80ae-110">參數</span><span class="sxs-lookup"><span data-stu-id="c80ae-110">PARAMETERS</span></span>

### <span data-ttu-id="c80ae-111">-內容</span><span class="sxs-lookup"><span data-stu-id="c80ae-111">-Context</span></span>
<span data-ttu-id="c80ae-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="c80ae-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c80ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c80ae-113">-DefaultProfile</span></span>
<span data-ttu-id="c80ae-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c80ae-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="c80ae-115">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="c80ae-115">-ExpiresOn</span></span>
<span data-ttu-id="c80ae-116">指定訂閱到期日。</span><span class="sxs-lookup"><span data-stu-id="c80ae-116">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="c80ae-117">此參數的預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="c80ae-117">The default value of this parameter is $Null.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c80ae-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="c80ae-118">-Name</span></span>
<span data-ttu-id="c80ae-119">指定訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="c80ae-119">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="c80ae-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c80ae-120">-PassThru</span></span>
<span data-ttu-id="c80ae-121">passthru</span><span class="sxs-lookup"><span data-stu-id="c80ae-121">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c80ae-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="c80ae-122">-PrimaryKey</span></span>
<span data-ttu-id="c80ae-123">指定訂閱主鍵。</span><span class="sxs-lookup"><span data-stu-id="c80ae-123">Specifies the subscription primary key.</span></span>
<span data-ttu-id="c80ae-124">如果沒有指定，則會自動產生此參數。</span><span class="sxs-lookup"><span data-stu-id="c80ae-124">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="c80ae-125">這個參數必須是1到300個字元長。</span><span class="sxs-lookup"><span data-stu-id="c80ae-125">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="c80ae-126">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="c80ae-126">-SecondaryKey</span></span>
<span data-ttu-id="c80ae-127">指定訂閱次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="c80ae-127">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="c80ae-128">如果沒有指定，則會自動產生此參數。</span><span class="sxs-lookup"><span data-stu-id="c80ae-128">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="c80ae-129">這個參數必須是1到300個字元長。</span><span class="sxs-lookup"><span data-stu-id="c80ae-129">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="c80ae-130">-State</span><span class="sxs-lookup"><span data-stu-id="c80ae-130">-State</span></span>
<span data-ttu-id="c80ae-131">指定訂閱狀態。</span><span class="sxs-lookup"><span data-stu-id="c80ae-131">Specifies the subscription state.</span></span>
<span data-ttu-id="c80ae-132">此參數的預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="c80ae-132">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="c80ae-133">-StateComment</span><span class="sxs-lookup"><span data-stu-id="c80ae-133">-StateComment</span></span>
<span data-ttu-id="c80ae-134">指定訂閱狀態批註。</span><span class="sxs-lookup"><span data-stu-id="c80ae-134">Specifies the subscription state comment.</span></span>
<span data-ttu-id="c80ae-135">此參數的預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="c80ae-135">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="c80ae-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c80ae-136">-SubscriptionId</span></span>
<span data-ttu-id="c80ae-137">指定訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="c80ae-137">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="c80ae-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c80ae-138">CommonParameters</span></span>
<span data-ttu-id="c80ae-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c80ae-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c80ae-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c80ae-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c80ae-141">輸入</span><span class="sxs-lookup"><span data-stu-id="c80ae-141">INPUTS</span></span>

### <span data-ttu-id="c80ae-142">所有</span><span class="sxs-lookup"><span data-stu-id="c80ae-142">None</span></span>
<span data-ttu-id="c80ae-143">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="c80ae-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c80ae-144">輸出</span><span class="sxs-lookup"><span data-stu-id="c80ae-144">OUTPUTS</span></span>

### <span data-ttu-id="c80ae-145">ServiceManagement. PsApiManagementSubscripition （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="c80ae-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscripition</span></span>

## <span data-ttu-id="c80ae-146">筆記</span><span class="sxs-lookup"><span data-stu-id="c80ae-146">NOTES</span></span>

## <span data-ttu-id="c80ae-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="c80ae-147">RELATED LINKS</span></span>

[<span data-ttu-id="c80ae-148">AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c80ae-148">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="c80ae-149">新-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c80ae-149">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="c80ae-150">移除-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c80ae-150">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)



---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 3b6d07577a6df05a57ed7675f5d14c847e8c33fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446894"
---
# <span data-ttu-id="40042-101">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="40042-101">Set-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="40042-102">摘要</span><span class="sxs-lookup"><span data-stu-id="40042-102">SYNOPSIS</span></span>
<span data-ttu-id="40042-103">設定現有的訂閱詳細資料。</span><span class="sxs-lookup"><span data-stu-id="40042-103">Sets existing subscription details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40042-104">句法</span><span class="sxs-lookup"><span data-stu-id="40042-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="40042-105">說明</span><span class="sxs-lookup"><span data-stu-id="40042-105">DESCRIPTION</span></span>
<span data-ttu-id="40042-106">**AzureRmApiManagementSubscription** Cmdlet 會設定現有的訂閱詳細資料。</span><span class="sxs-lookup"><span data-stu-id="40042-106">The **Set-AzureRmApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="40042-107">示例</span><span class="sxs-lookup"><span data-stu-id="40042-107">EXAMPLES</span></span>

### <span data-ttu-id="40042-108">範例1：設定訂閱的狀態與主要和次要金鑰</span><span class="sxs-lookup"><span data-stu-id="40042-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>Set-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SencondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="40042-109">這個命令會設定訂閱的主要和次要金鑰，並啟用。</span><span class="sxs-lookup"><span data-stu-id="40042-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="40042-110">參數</span><span class="sxs-lookup"><span data-stu-id="40042-110">PARAMETERS</span></span>

### <span data-ttu-id="40042-111">-內容</span><span class="sxs-lookup"><span data-stu-id="40042-111">-Context</span></span>
<span data-ttu-id="40042-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="40042-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40042-113">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="40042-113">-ExpiresOn</span></span>
<span data-ttu-id="40042-114">指定訂閱到期日。</span><span class="sxs-lookup"><span data-stu-id="40042-114">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="40042-115">此參數的預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="40042-115">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40042-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="40042-116">-Name</span></span>
<span data-ttu-id="40042-117">指定訂閱名稱。</span><span class="sxs-lookup"><span data-stu-id="40042-117">Specifies a subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40042-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40042-118">-PassThru</span></span>
<span data-ttu-id="40042-119">passthru</span><span class="sxs-lookup"><span data-stu-id="40042-119">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40042-120">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="40042-120">-PrimaryKey</span></span>
<span data-ttu-id="40042-121">指定訂閱主鍵。</span><span class="sxs-lookup"><span data-stu-id="40042-121">Specifies the subscription primary key.</span></span>
<span data-ttu-id="40042-122">如果沒有指定，則會自動產生此參數。</span><span class="sxs-lookup"><span data-stu-id="40042-122">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="40042-123">這個參數必須是1到300個字元長。</span><span class="sxs-lookup"><span data-stu-id="40042-123">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40042-124">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="40042-124">-SecondaryKey</span></span>
<span data-ttu-id="40042-125">指定訂閱次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="40042-125">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="40042-126">如果沒有指定，則會自動產生此參數。</span><span class="sxs-lookup"><span data-stu-id="40042-126">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="40042-127">這個參數必須是1到300個字元長。</span><span class="sxs-lookup"><span data-stu-id="40042-127">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40042-128">-State</span><span class="sxs-lookup"><span data-stu-id="40042-128">-State</span></span>
<span data-ttu-id="40042-129">指定訂閱狀態。</span><span class="sxs-lookup"><span data-stu-id="40042-129">Specifies the subscription state.</span></span>
<span data-ttu-id="40042-130">此參數的預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="40042-130">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState]
Parameter Sets: (All)
Aliases: 
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40042-131">-StateComment</span><span class="sxs-lookup"><span data-stu-id="40042-131">-StateComment</span></span>
<span data-ttu-id="40042-132">指定訂閱狀態批註。</span><span class="sxs-lookup"><span data-stu-id="40042-132">Specifies the subscription state comment.</span></span>
<span data-ttu-id="40042-133">此參數的預設值為 [$Null]。</span><span class="sxs-lookup"><span data-stu-id="40042-133">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40042-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="40042-134">-SubscriptionId</span></span>
<span data-ttu-id="40042-135">指定訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="40042-135">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="40042-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40042-136">-DefaultProfile</span></span>
<span data-ttu-id="40042-137">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="40042-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40042-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40042-138">CommonParameters</span></span>
<span data-ttu-id="40042-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="40042-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40042-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="40042-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40042-141">輸入</span><span class="sxs-lookup"><span data-stu-id="40042-141">INPUTS</span></span>

## <span data-ttu-id="40042-142">輸出</span><span class="sxs-lookup"><span data-stu-id="40042-142">OUTPUTS</span></span>

### <span data-ttu-id="40042-143">ServiceManagement. PsApiManagementSubscripition （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="40042-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscripition</span></span>

## <span data-ttu-id="40042-144">筆記</span><span class="sxs-lookup"><span data-stu-id="40042-144">NOTES</span></span>

## <span data-ttu-id="40042-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="40042-145">RELATED LINKS</span></span>

[<span data-ttu-id="40042-146">AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="40042-146">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="40042-147">新-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="40042-147">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="40042-148">移除-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="40042-148">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)



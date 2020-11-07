---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 777d71dec17f75cba84c15c7499e5ec56ffb854a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626571"
---
# <span data-ttu-id="0d8a4-101">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0d8a4-101">Remove-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="0d8a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0d8a4-102">SYNOPSIS</span></span>
<span data-ttu-id="0d8a4-103">刪除現有的訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d8a4-103">Deletes an existing subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d8a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="0d8a4-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d8a4-105">說明</span><span class="sxs-lookup"><span data-stu-id="0d8a4-105">DESCRIPTION</span></span>
<span data-ttu-id="0d8a4-106">AzureRmApiManagementSubscription Cmdlet 會刪除現有 **的** 訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d8a4-106">The **Remove-AzureRmApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="0d8a4-107">示例</span><span class="sxs-lookup"><span data-stu-id="0d8a4-107">EXAMPLES</span></span>

### <span data-ttu-id="0d8a4-108">範例1：刪除訂閱</span><span class="sxs-lookup"><span data-stu-id="0d8a4-108">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="0d8a4-109">這個命令會刪除現有的訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d8a4-109">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="0d8a4-110">參數</span><span class="sxs-lookup"><span data-stu-id="0d8a4-110">PARAMETERS</span></span>

### <span data-ttu-id="0d8a4-111">-內容</span><span class="sxs-lookup"><span data-stu-id="0d8a4-111">-Context</span></span>
<span data-ttu-id="0d8a4-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="0d8a4-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0d8a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d8a4-113">-DefaultProfile</span></span>
<span data-ttu-id="0d8a4-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d8a4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="0d8a4-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d8a4-115">-PassThru</span></span>
<span data-ttu-id="0d8a4-116">指示這個 Cmdlet 會傳回 $True 的值（如果它成功的話），否則傳回 $false 的值。</span><span class="sxs-lookup"><span data-stu-id="0d8a4-116">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="0d8a4-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0d8a4-117">-SubscriptionId</span></span>
<span data-ttu-id="0d8a4-118">指定訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="0d8a4-118">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="0d8a4-119">-確認</span><span class="sxs-lookup"><span data-stu-id="0d8a4-119">-Confirm</span></span>
<span data-ttu-id="0d8a4-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0d8a4-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8a4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d8a4-121">-WhatIf</span></span>
<span data-ttu-id="0d8a4-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0d8a4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d8a4-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0d8a4-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d8a4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d8a4-124">CommonParameters</span></span>
<span data-ttu-id="0d8a4-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0d8a4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d8a4-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0d8a4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d8a4-127">輸入</span><span class="sxs-lookup"><span data-stu-id="0d8a4-127">INPUTS</span></span>

### <span data-ttu-id="0d8a4-128">所有</span><span class="sxs-lookup"><span data-stu-id="0d8a4-128">None</span></span>
<span data-ttu-id="0d8a4-129">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="0d8a4-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0d8a4-130">輸出</span><span class="sxs-lookup"><span data-stu-id="0d8a4-130">OUTPUTS</span></span>

### <span data-ttu-id="0d8a4-131">布林值</span><span class="sxs-lookup"><span data-stu-id="0d8a4-131">Boolean</span></span>

## <span data-ttu-id="0d8a4-132">筆記</span><span class="sxs-lookup"><span data-stu-id="0d8a4-132">NOTES</span></span>

## <span data-ttu-id="0d8a4-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d8a4-133">RELATED LINKS</span></span>

[<span data-ttu-id="0d8a4-134">AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0d8a4-134">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="0d8a4-135">新-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0d8a4-135">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="0d8a4-136">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0d8a4-136">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)



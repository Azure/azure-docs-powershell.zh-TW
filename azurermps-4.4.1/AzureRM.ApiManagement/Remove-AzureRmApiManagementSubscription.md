---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
ms.openlocfilehash: fd232a0f118db5730c41ef1588eaf07d80df69f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445175"
---
# <span data-ttu-id="3b8c7-101">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="3b8c7-101">Remove-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="3b8c7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3b8c7-102">SYNOPSIS</span></span>
<span data-ttu-id="3b8c7-103">刪除現有的訂閱。</span><span class="sxs-lookup"><span data-stu-id="3b8c7-103">Deletes an existing subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b8c7-104">句法</span><span class="sxs-lookup"><span data-stu-id="3b8c7-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b8c7-105">說明</span><span class="sxs-lookup"><span data-stu-id="3b8c7-105">DESCRIPTION</span></span>
<span data-ttu-id="3b8c7-106">AzureRmApiManagementSubscription Cmdlet 會刪除現有 **的** 訂閱。</span><span class="sxs-lookup"><span data-stu-id="3b8c7-106">The **Remove-AzureRmApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="3b8c7-107">示例</span><span class="sxs-lookup"><span data-stu-id="3b8c7-107">EXAMPLES</span></span>

### <span data-ttu-id="3b8c7-108">範例1：刪除訂閱</span><span class="sxs-lookup"><span data-stu-id="3b8c7-108">Example 1: Delete a subscription</span></span>
```
PS C:\>Remove-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="3b8c7-109">這個命令會刪除現有的訂閱。</span><span class="sxs-lookup"><span data-stu-id="3b8c7-109">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="3b8c7-110">參數</span><span class="sxs-lookup"><span data-stu-id="3b8c7-110">PARAMETERS</span></span>

### <span data-ttu-id="3b8c7-111">-內容</span><span class="sxs-lookup"><span data-stu-id="3b8c7-111">-Context</span></span>
<span data-ttu-id="3b8c7-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="3b8c7-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3b8c7-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b8c7-113">-PassThru</span></span>
<span data-ttu-id="3b8c7-114">指示這個 Cmdlet 會傳回 $True 的值（如果它成功的話），否則傳回 $false 的值。</span><span class="sxs-lookup"><span data-stu-id="3b8c7-114">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="3b8c7-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3b8c7-115">-SubscriptionId</span></span>
<span data-ttu-id="3b8c7-116">指定訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="3b8c7-116">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="3b8c7-117">-確認</span><span class="sxs-lookup"><span data-stu-id="3b8c7-117">-Confirm</span></span>
<span data-ttu-id="3b8c7-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3b8c7-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b8c7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b8c7-119">-WhatIf</span></span>
<span data-ttu-id="3b8c7-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3b8c7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b8c7-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3b8c7-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b8c7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b8c7-122">-DefaultProfile</span></span>
<span data-ttu-id="3b8c7-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3b8c7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b8c7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b8c7-124">CommonParameters</span></span>
<span data-ttu-id="3b8c7-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3b8c7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b8c7-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3b8c7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b8c7-127">輸入</span><span class="sxs-lookup"><span data-stu-id="3b8c7-127">INPUTS</span></span>

## <span data-ttu-id="3b8c7-128">輸出</span><span class="sxs-lookup"><span data-stu-id="3b8c7-128">OUTPUTS</span></span>

### <span data-ttu-id="3b8c7-129">布林值</span><span class="sxs-lookup"><span data-stu-id="3b8c7-129">Boolean</span></span>

## <span data-ttu-id="3b8c7-130">筆記</span><span class="sxs-lookup"><span data-stu-id="3b8c7-130">NOTES</span></span>

## <span data-ttu-id="3b8c7-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b8c7-131">RELATED LINKS</span></span>

[<span data-ttu-id="3b8c7-132">AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="3b8c7-132">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="3b8c7-133">新-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="3b8c7-133">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="3b8c7-134">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="3b8c7-134">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)



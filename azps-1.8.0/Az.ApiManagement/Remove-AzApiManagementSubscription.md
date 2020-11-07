---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
ms.openlocfilehash: 411fa67d81b772c2e9dcd6b1690e8eac50de3ea0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788817"
---
# <span data-ttu-id="4810a-101">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4810a-101">Remove-AzApiManagementSubscription</span></span>

## <span data-ttu-id="4810a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4810a-102">SYNOPSIS</span></span>
<span data-ttu-id="4810a-103">刪除現有的訂閱。</span><span class="sxs-lookup"><span data-stu-id="4810a-103">Deletes an existing subscription.</span></span>

## <span data-ttu-id="4810a-104">句法</span><span class="sxs-lookup"><span data-stu-id="4810a-104">SYNTAX</span></span>

```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4810a-105">說明</span><span class="sxs-lookup"><span data-stu-id="4810a-105">DESCRIPTION</span></span>
<span data-ttu-id="4810a-106">AzApiManagementSubscription Cmdlet 會刪除現有 **的** 訂閱。</span><span class="sxs-lookup"><span data-stu-id="4810a-106">The **Remove-AzApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="4810a-107">示例</span><span class="sxs-lookup"><span data-stu-id="4810a-107">EXAMPLES</span></span>

### <span data-ttu-id="4810a-108">範例1：刪除訂閱</span><span class="sxs-lookup"><span data-stu-id="4810a-108">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="4810a-109">這個命令會刪除現有的訂閱。</span><span class="sxs-lookup"><span data-stu-id="4810a-109">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="4810a-110">參數</span><span class="sxs-lookup"><span data-stu-id="4810a-110">PARAMETERS</span></span>

### <span data-ttu-id="4810a-111">-內容</span><span class="sxs-lookup"><span data-stu-id="4810a-111">-Context</span></span>
<span data-ttu-id="4810a-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="4810a-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4810a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4810a-113">-DefaultProfile</span></span>
<span data-ttu-id="4810a-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4810a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4810a-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4810a-115">-PassThru</span></span>
<span data-ttu-id="4810a-116">指示這個 Cmdlet 會傳回 $True 的值（如果它成功的話），否則傳回 $false 的值。</span><span class="sxs-lookup"><span data-stu-id="4810a-116">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="4810a-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4810a-117">-SubscriptionId</span></span>
<span data-ttu-id="4810a-118">指定訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="4810a-118">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="4810a-119">-確認</span><span class="sxs-lookup"><span data-stu-id="4810a-119">-Confirm</span></span>
<span data-ttu-id="4810a-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4810a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4810a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4810a-121">-WhatIf</span></span>
<span data-ttu-id="4810a-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4810a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4810a-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4810a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4810a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4810a-124">CommonParameters</span></span>
<span data-ttu-id="4810a-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4810a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4810a-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4810a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4810a-127">輸入</span><span class="sxs-lookup"><span data-stu-id="4810a-127">INPUTS</span></span>

### <span data-ttu-id="4810a-128">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="4810a-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4810a-129">System.object</span><span class="sxs-lookup"><span data-stu-id="4810a-129">System.String</span></span>

### <span data-ttu-id="4810a-130">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="4810a-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4810a-131">輸出</span><span class="sxs-lookup"><span data-stu-id="4810a-131">OUTPUTS</span></span>

### <span data-ttu-id="4810a-132">System.object</span><span class="sxs-lookup"><span data-stu-id="4810a-132">System.Boolean</span></span>

## <span data-ttu-id="4810a-133">筆記</span><span class="sxs-lookup"><span data-stu-id="4810a-133">NOTES</span></span>

## <span data-ttu-id="4810a-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="4810a-134">RELATED LINKS</span></span>

[<span data-ttu-id="4810a-135">AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4810a-135">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="4810a-136">新-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4810a-136">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="4810a-137">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="4810a-137">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)



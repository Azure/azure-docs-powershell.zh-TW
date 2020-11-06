---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: ecbb2b6671f1482f31cb7b3f0b07d4e9be4bbb3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447197"
---
# <span data-ttu-id="cd537-101">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="cd537-101">Remove-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="cd537-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cd537-102">SYNOPSIS</span></span>
<span data-ttu-id="cd537-103">移除現有的身分識別提供者配置。</span><span class="sxs-lookup"><span data-stu-id="cd537-103">Removes an existing Identity Provider Configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd537-104">句法</span><span class="sxs-lookup"><span data-stu-id="cd537-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd537-105">說明</span><span class="sxs-lookup"><span data-stu-id="cd537-105">DESCRIPTION</span></span>
<span data-ttu-id="cd537-106">移除現有的身分識別提供者配置。</span><span class="sxs-lookup"><span data-stu-id="cd537-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="cd537-107">示例</span><span class="sxs-lookup"><span data-stu-id="cd537-107">EXAMPLES</span></span>

### <span data-ttu-id="cd537-108">從 ApiManagement service 中移除 Facebook 身分識別提供者設定</span><span class="sxs-lookup"><span data-stu-id="cd537-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
Remove-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="cd537-109">刪除與 Facebook 身分識別提供者配置相關的設定。</span><span class="sxs-lookup"><span data-stu-id="cd537-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="cd537-110">參數</span><span class="sxs-lookup"><span data-stu-id="cd537-110">PARAMETERS</span></span>

### <span data-ttu-id="cd537-111">-內容</span><span class="sxs-lookup"><span data-stu-id="cd537-111">-Context</span></span>
<span data-ttu-id="cd537-112">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="cd537-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="cd537-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="cd537-113">This parameter is required.</span></span>

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

### <span data-ttu-id="cd537-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd537-114">-PassThru</span></span>
<span data-ttu-id="cd537-115">指示這個 Cmdlet 會傳回 $True 的值（如果操作成功或 $False 則不然）。</span><span class="sxs-lookup"><span data-stu-id="cd537-115">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>


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

### <span data-ttu-id="cd537-116">-類型</span><span class="sxs-lookup"><span data-stu-id="cd537-116">-Type</span></span>
<span data-ttu-id="cd537-117">現有身分識別提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cd537-117">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="cd537-118">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="cd537-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd537-119">-確認</span><span class="sxs-lookup"><span data-stu-id="cd537-119">-Confirm</span></span>
<span data-ttu-id="cd537-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cd537-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd537-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd537-121">-WhatIf</span></span>
<span data-ttu-id="cd537-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cd537-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd537-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd537-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd537-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd537-124">-DefaultProfile</span></span>
<span data-ttu-id="cd537-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cd537-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd537-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd537-126">CommonParameters</span></span>
<span data-ttu-id="cd537-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cd537-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd537-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cd537-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd537-129">輸入</span><span class="sxs-lookup"><span data-stu-id="cd537-129">INPUTS</span></span>

## <span data-ttu-id="cd537-130">輸出</span><span class="sxs-lookup"><span data-stu-id="cd537-130">OUTPUTS</span></span>

### <span data-ttu-id="cd537-131">bool</span><span class="sxs-lookup"><span data-stu-id="cd537-131">bool</span></span>

## <span data-ttu-id="cd537-132">筆記</span><span class="sxs-lookup"><span data-stu-id="cd537-132">NOTES</span></span>

## <span data-ttu-id="cd537-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="cd537-133">RELATED LINKS</span></span>

[<span data-ttu-id="cd537-134">新-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="cd537-134">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="cd537-135">AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="cd537-135">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="cd537-136">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="cd537-136">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)


---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: d8cc54570b1282889a93c803e1216096cde35b27
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444107"
---
# <span data-ttu-id="7b2e9-101">Remove-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="7b2e9-101">Remove-AzureRmApiManagementIdentityProvider</span></span>

## <span data-ttu-id="7b2e9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7b2e9-102">SYNOPSIS</span></span>
<span data-ttu-id="7b2e9-103">移除現有的身分識別提供者配置。</span><span class="sxs-lookup"><span data-stu-id="7b2e9-103">Removes an existing Identity Provider Configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b2e9-104">句法</span><span class="sxs-lookup"><span data-stu-id="7b2e9-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b2e9-105">說明</span><span class="sxs-lookup"><span data-stu-id="7b2e9-105">DESCRIPTION</span></span>
<span data-ttu-id="7b2e9-106">移除現有的身分識別提供者配置。</span><span class="sxs-lookup"><span data-stu-id="7b2e9-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="7b2e9-107">示例</span><span class="sxs-lookup"><span data-stu-id="7b2e9-107">EXAMPLES</span></span>

### <span data-ttu-id="7b2e9-108">從 ApiManagement service 中移除 Facebook 身分識別提供者設定</span><span class="sxs-lookup"><span data-stu-id="7b2e9-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="7b2e9-109">刪除與 Facebook 身分識別提供者配置相關的設定。</span><span class="sxs-lookup"><span data-stu-id="7b2e9-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="7b2e9-110">參數</span><span class="sxs-lookup"><span data-stu-id="7b2e9-110">PARAMETERS</span></span>

### <span data-ttu-id="7b2e9-111">-內容</span><span class="sxs-lookup"><span data-stu-id="7b2e9-111">-Context</span></span>
<span data-ttu-id="7b2e9-112">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="7b2e9-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7b2e9-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="7b2e9-113">This parameter is required.</span></span>

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

### <span data-ttu-id="7b2e9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b2e9-114">-DefaultProfile</span></span>
<span data-ttu-id="7b2e9-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7b2e9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b2e9-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b2e9-116">-PassThru</span></span>
<span data-ttu-id="7b2e9-117">指示這個 Cmdlet 會傳回 $True 的值（如果操作成功或 $False 則不然）。</span><span class="sxs-lookup"><span data-stu-id="7b2e9-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="7b2e9-118">-類型</span><span class="sxs-lookup"><span data-stu-id="7b2e9-118">-Type</span></span>
<span data-ttu-id="7b2e9-119">現有身分識別提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7b2e9-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="7b2e9-120">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="7b2e9-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b2e9-121">-確認</span><span class="sxs-lookup"><span data-stu-id="7b2e9-121">-Confirm</span></span>
<span data-ttu-id="7b2e9-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7b2e9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b2e9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b2e9-123">-WhatIf</span></span>
<span data-ttu-id="7b2e9-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7b2e9-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b2e9-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7b2e9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b2e9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b2e9-126">CommonParameters</span></span>
<span data-ttu-id="7b2e9-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7b2e9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b2e9-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7b2e9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b2e9-129">輸入</span><span class="sxs-lookup"><span data-stu-id="7b2e9-129">INPUTS</span></span>

### <span data-ttu-id="7b2e9-130">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="7b2e9-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7b2e9-131">ServiceManagement. PsApiManagementIdentityProviderType （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="7b2e9-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="7b2e9-132">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="7b2e9-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7b2e9-133">輸出</span><span class="sxs-lookup"><span data-stu-id="7b2e9-133">OUTPUTS</span></span>

### <span data-ttu-id="7b2e9-134">System.object</span><span class="sxs-lookup"><span data-stu-id="7b2e9-134">System.Boolean</span></span>

## <span data-ttu-id="7b2e9-135">筆記</span><span class="sxs-lookup"><span data-stu-id="7b2e9-135">NOTES</span></span>

## <span data-ttu-id="7b2e9-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="7b2e9-136">RELATED LINKS</span></span>

[<span data-ttu-id="7b2e9-137">新-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="7b2e9-137">New-AzureRmApiManagementIdentityProvider</span></span>](./New-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="7b2e9-138">AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="7b2e9-138">Get-AzureRmApiManagementIdentityProvider</span></span>](./Get-AzureRmApiManagementIdentityProvider.md)

[<span data-ttu-id="7b2e9-139">Set-AzureRmApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="7b2e9-139">Set-AzureRmApiManagementIdentityProvider</span></span>](./Set-AzureRmApiManagementIdentityProvider.md)


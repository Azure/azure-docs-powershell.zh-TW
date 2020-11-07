---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 5258b041f2858ce766f5b6e932412986545ccf13
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788849"
---
# <span data-ttu-id="0b4e2-101">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="0b4e2-101">Remove-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="0b4e2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0b4e2-102">SYNOPSIS</span></span>
<span data-ttu-id="0b4e2-103">移除現有的身分識別提供者配置。</span><span class="sxs-lookup"><span data-stu-id="0b4e2-103">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="0b4e2-104">句法</span><span class="sxs-lookup"><span data-stu-id="0b4e2-104">SYNTAX</span></span>

```
Remove-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b4e2-105">說明</span><span class="sxs-lookup"><span data-stu-id="0b4e2-105">DESCRIPTION</span></span>
<span data-ttu-id="0b4e2-106">移除現有的身分識別提供者配置。</span><span class="sxs-lookup"><span data-stu-id="0b4e2-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="0b4e2-107">示例</span><span class="sxs-lookup"><span data-stu-id="0b4e2-107">EXAMPLES</span></span>

### <span data-ttu-id="0b4e2-108">從 ApiManagement service 中移除 Facebook 身分識別提供者設定</span><span class="sxs-lookup"><span data-stu-id="0b4e2-108">Removes the Facebook identity provider settings from ApiManagement service</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="0b4e2-109">刪除與 Facebook 身分識別提供者配置相關的設定。</span><span class="sxs-lookup"><span data-stu-id="0b4e2-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="0b4e2-110">參數</span><span class="sxs-lookup"><span data-stu-id="0b4e2-110">PARAMETERS</span></span>

### <span data-ttu-id="0b4e2-111">-內容</span><span class="sxs-lookup"><span data-stu-id="0b4e2-111">-Context</span></span>
<span data-ttu-id="0b4e2-112">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="0b4e2-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0b4e2-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="0b4e2-113">This parameter is required.</span></span>

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

### <span data-ttu-id="0b4e2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b4e2-114">-DefaultProfile</span></span>
<span data-ttu-id="0b4e2-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0b4e2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b4e2-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b4e2-116">-PassThru</span></span>
<span data-ttu-id="0b4e2-117">指示這個 Cmdlet 會傳回 $True 的值（如果操作成功或 $False 則不然）。</span><span class="sxs-lookup"><span data-stu-id="0b4e2-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="0b4e2-118">-類型</span><span class="sxs-lookup"><span data-stu-id="0b4e2-118">-Type</span></span>
<span data-ttu-id="0b4e2-119">現有身分識別提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0b4e2-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="0b4e2-120">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="0b4e2-120">This parameter is required.</span></span>

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

### <span data-ttu-id="0b4e2-121">-確認</span><span class="sxs-lookup"><span data-stu-id="0b4e2-121">-Confirm</span></span>
<span data-ttu-id="0b4e2-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0b4e2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b4e2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b4e2-123">-WhatIf</span></span>
<span data-ttu-id="0b4e2-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0b4e2-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b4e2-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0b4e2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b4e2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b4e2-126">CommonParameters</span></span>
<span data-ttu-id="0b4e2-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0b4e2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b4e2-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0b4e2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b4e2-129">輸入</span><span class="sxs-lookup"><span data-stu-id="0b4e2-129">INPUTS</span></span>

### <span data-ttu-id="0b4e2-130">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="0b4e2-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0b4e2-131">ServiceManagement. PsApiManagementIdentityProviderType （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="0b4e2-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="0b4e2-132">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="0b4e2-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0b4e2-133">輸出</span><span class="sxs-lookup"><span data-stu-id="0b4e2-133">OUTPUTS</span></span>

### <span data-ttu-id="0b4e2-134">System.object</span><span class="sxs-lookup"><span data-stu-id="0b4e2-134">System.Boolean</span></span>

## <span data-ttu-id="0b4e2-135">筆記</span><span class="sxs-lookup"><span data-stu-id="0b4e2-135">NOTES</span></span>

## <span data-ttu-id="0b4e2-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b4e2-136">RELATED LINKS</span></span>

[<span data-ttu-id="0b4e2-137">新-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="0b4e2-137">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="0b4e2-138">AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="0b4e2-138">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="0b4e2-139">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="0b4e2-139">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementIdentityProvider.md
ms.openlocfilehash: f80fe2b09be6d4bdc624f65de014d3b7f1beadd6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917805"
---
# <span data-ttu-id="91b83-101">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="91b83-101">Remove-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="91b83-102">簡介</span><span class="sxs-lookup"><span data-stu-id="91b83-102">SYNOPSIS</span></span>
<span data-ttu-id="91b83-103">移除現有的身分識別提供者組配置。</span><span class="sxs-lookup"><span data-stu-id="91b83-103">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="91b83-104">語法</span><span class="sxs-lookup"><span data-stu-id="91b83-104">SYNTAX</span></span>

```
Remove-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91b83-105">描述</span><span class="sxs-lookup"><span data-stu-id="91b83-105">DESCRIPTION</span></span>
<span data-ttu-id="91b83-106">移除現有的身分識別提供者組配置。</span><span class="sxs-lookup"><span data-stu-id="91b83-106">Removes an existing Identity Provider Configuration.</span></span>

## <span data-ttu-id="91b83-107">例子</span><span class="sxs-lookup"><span data-stu-id="91b83-107">EXAMPLES</span></span>

### <span data-ttu-id="91b83-108">範例 1：從 ApiManagement 服務移除 Facebook 身分識別提供者設定</span><span class="sxs-lookup"><span data-stu-id="91b83-108">Example 1: Removes the Facebook identity provider settings from ApiManagement service</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -PassThru
```

<span data-ttu-id="91b83-109">刪除與 Facebook 身分識別提供者組配置的關聯。</span><span class="sxs-lookup"><span data-stu-id="91b83-109">Deletes configuration related to Facebook Identity provider configuration.</span></span>

## <span data-ttu-id="91b83-110">參數</span><span class="sxs-lookup"><span data-stu-id="91b83-110">PARAMETERS</span></span>

### <span data-ttu-id="91b83-111">-內容</span><span class="sxs-lookup"><span data-stu-id="91b83-111">-Context</span></span>
<span data-ttu-id="91b83-112">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="91b83-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="91b83-113">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="91b83-113">This parameter is required.</span></span>

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

### <span data-ttu-id="91b83-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91b83-114">-DefaultProfile</span></span>
<span data-ttu-id="91b83-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="91b83-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91b83-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91b83-116">-PassThru</span></span>
<span data-ttu-id="91b83-117">表示此 Cmdlet 會當作業成功或$True時，會$False值。</span><span class="sxs-lookup"><span data-stu-id="91b83-117">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="91b83-118">-類型</span><span class="sxs-lookup"><span data-stu-id="91b83-118">-Type</span></span>
<span data-ttu-id="91b83-119">現有身分識別提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="91b83-119">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="91b83-120">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="91b83-120">This parameter is required.</span></span>

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

### <span data-ttu-id="91b83-121">-確認</span><span class="sxs-lookup"><span data-stu-id="91b83-121">-Confirm</span></span>
<span data-ttu-id="91b83-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="91b83-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91b83-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91b83-123">-WhatIf</span></span>
<span data-ttu-id="91b83-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="91b83-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91b83-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="91b83-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91b83-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91b83-126">CommonParameters</span></span>
<span data-ttu-id="91b83-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="91b83-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91b83-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91b83-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91b83-129">輸入</span><span class="sxs-lookup"><span data-stu-id="91b83-129">INPUTS</span></span>

### <span data-ttu-id="91b83-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="91b83-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="91b83-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="91b83-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="91b83-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="91b83-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="91b83-133">輸出</span><span class="sxs-lookup"><span data-stu-id="91b83-133">OUTPUTS</span></span>

### <span data-ttu-id="91b83-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="91b83-134">System.Boolean</span></span>

## <span data-ttu-id="91b83-135">筆記</span><span class="sxs-lookup"><span data-stu-id="91b83-135">NOTES</span></span>

## <span data-ttu-id="91b83-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="91b83-136">RELATED LINKS</span></span>

[<span data-ttu-id="91b83-137">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="91b83-137">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="91b83-138">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="91b83-138">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="91b83-139">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="91b83-139">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)


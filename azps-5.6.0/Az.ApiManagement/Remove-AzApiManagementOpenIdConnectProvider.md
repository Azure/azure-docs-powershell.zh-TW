---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 3d7d6600e7e26202c920499a615f4124767c830c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911198"
---
# <span data-ttu-id="70b21-101">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="70b21-101">Remove-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="70b21-102">簡介</span><span class="sxs-lookup"><span data-stu-id="70b21-102">SYNOPSIS</span></span>
<span data-ttu-id="70b21-103">移除 OpenID Connect 提供者。</span><span class="sxs-lookup"><span data-stu-id="70b21-103">Removes an OpenID Connect provider.</span></span>

## <span data-ttu-id="70b21-104">語法</span><span class="sxs-lookup"><span data-stu-id="70b21-104">SYNTAX</span></span>

```
Remove-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70b21-105">描述</span><span class="sxs-lookup"><span data-stu-id="70b21-105">DESCRIPTION</span></span>
<span data-ttu-id="70b21-106">**Remove-AzApiManagementOpenIdConnectProvider Cmdlet** 會移除 Azure API 管理的 OpenID Connect 提供者。</span><span class="sxs-lookup"><span data-stu-id="70b21-106">The **Remove-AzApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="70b21-107">例子</span><span class="sxs-lookup"><span data-stu-id="70b21-107">EXAMPLES</span></span>

### <span data-ttu-id="70b21-108">範例 1：移除提供者</span><span class="sxs-lookup"><span data-stu-id="70b21-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -PassThru
```

<span data-ttu-id="70b21-109">此命令會移除具有識別碼為 ISPPROvider01 的提供者。</span><span class="sxs-lookup"><span data-stu-id="70b21-109">This command removes a provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="70b21-110">參數</span><span class="sxs-lookup"><span data-stu-id="70b21-110">PARAMETERS</span></span>

### <span data-ttu-id="70b21-111">-內容</span><span class="sxs-lookup"><span data-stu-id="70b21-111">-Context</span></span>
<span data-ttu-id="70b21-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="70b21-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="70b21-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70b21-113">-DefaultProfile</span></span>
<span data-ttu-id="70b21-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="70b21-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70b21-115">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="70b21-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="70b21-116">指定此 Cmdlet 移除的提供者識別碼。</span><span class="sxs-lookup"><span data-stu-id="70b21-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="70b21-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70b21-117">-PassThru</span></span>
<span data-ttu-id="70b21-118">表示此 Cmdlet 會當作業成功或$True時，會$False值。</span><span class="sxs-lookup"><span data-stu-id="70b21-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="70b21-119">-確認</span><span class="sxs-lookup"><span data-stu-id="70b21-119">-Confirm</span></span>
<span data-ttu-id="70b21-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="70b21-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70b21-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70b21-121">-WhatIf</span></span>
<span data-ttu-id="70b21-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="70b21-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70b21-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="70b21-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70b21-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70b21-124">CommonParameters</span></span>
<span data-ttu-id="70b21-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="70b21-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70b21-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70b21-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70b21-127">輸入</span><span class="sxs-lookup"><span data-stu-id="70b21-127">INPUTS</span></span>

### <span data-ttu-id="70b21-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="70b21-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="70b21-129">System.String</span><span class="sxs-lookup"><span data-stu-id="70b21-129">System.String</span></span>

### <span data-ttu-id="70b21-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="70b21-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="70b21-131">輸出</span><span class="sxs-lookup"><span data-stu-id="70b21-131">OUTPUTS</span></span>

### <span data-ttu-id="70b21-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="70b21-132">System.Boolean</span></span>

## <span data-ttu-id="70b21-133">筆記</span><span class="sxs-lookup"><span data-stu-id="70b21-133">NOTES</span></span>

## <span data-ttu-id="70b21-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="70b21-134">RELATED LINKS</span></span>

[<span data-ttu-id="70b21-135">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="70b21-135">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="70b21-136">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="70b21-136">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="70b21-137">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="70b21-137">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)



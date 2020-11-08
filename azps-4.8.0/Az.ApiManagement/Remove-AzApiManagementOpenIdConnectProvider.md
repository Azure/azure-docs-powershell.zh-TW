---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: ab278dcf56646463e1ccbc8ada9baa896b1759bf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969985"
---
# <span data-ttu-id="81469-101">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="81469-101">Remove-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="81469-102">摘要</span><span class="sxs-lookup"><span data-stu-id="81469-102">SYNOPSIS</span></span>
<span data-ttu-id="81469-103">移除 OpenID 連接提供者。</span><span class="sxs-lookup"><span data-stu-id="81469-103">Removes an OpenID Connect provider.</span></span>

## <span data-ttu-id="81469-104">句法</span><span class="sxs-lookup"><span data-stu-id="81469-104">SYNTAX</span></span>

```
Remove-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81469-105">說明</span><span class="sxs-lookup"><span data-stu-id="81469-105">DESCRIPTION</span></span>
<span data-ttu-id="81469-106">**AzApiManagementOpenIdConnectProvider** Cmdlet 會針對 Azure API 管理移除 OpenID 連接提供者。</span><span class="sxs-lookup"><span data-stu-id="81469-106">The **Remove-AzApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="81469-107">示例</span><span class="sxs-lookup"><span data-stu-id="81469-107">EXAMPLES</span></span>

### <span data-ttu-id="81469-108">範例1：移除提供者</span><span class="sxs-lookup"><span data-stu-id="81469-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -PassThru
```

<span data-ttu-id="81469-109">這個命令會移除 ID 為 OICProvider01 的提供者。</span><span class="sxs-lookup"><span data-stu-id="81469-109">This command removes a provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="81469-110">參數</span><span class="sxs-lookup"><span data-stu-id="81469-110">PARAMETERS</span></span>

### <span data-ttu-id="81469-111">-內容</span><span class="sxs-lookup"><span data-stu-id="81469-111">-Context</span></span>
<span data-ttu-id="81469-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="81469-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="81469-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81469-113">-DefaultProfile</span></span>
<span data-ttu-id="81469-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="81469-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81469-115">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="81469-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="81469-116">指定此 Cmdlet 移除之提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="81469-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="81469-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81469-117">-PassThru</span></span>
<span data-ttu-id="81469-118">指示這個 Cmdlet 會傳回 $True 的值（如果操作成功或 $False 則不然）。</span><span class="sxs-lookup"><span data-stu-id="81469-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="81469-119">-確認</span><span class="sxs-lookup"><span data-stu-id="81469-119">-Confirm</span></span>
<span data-ttu-id="81469-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="81469-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81469-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81469-121">-WhatIf</span></span>
<span data-ttu-id="81469-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="81469-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81469-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="81469-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81469-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81469-124">CommonParameters</span></span>
<span data-ttu-id="81469-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="81469-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81469-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="81469-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81469-127">輸入</span><span class="sxs-lookup"><span data-stu-id="81469-127">INPUTS</span></span>

### <span data-ttu-id="81469-128">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="81469-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="81469-129">System.object</span><span class="sxs-lookup"><span data-stu-id="81469-129">System.String</span></span>

### <span data-ttu-id="81469-130">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="81469-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="81469-131">輸出</span><span class="sxs-lookup"><span data-stu-id="81469-131">OUTPUTS</span></span>

### <span data-ttu-id="81469-132">System.object</span><span class="sxs-lookup"><span data-stu-id="81469-132">System.Boolean</span></span>

## <span data-ttu-id="81469-133">筆記</span><span class="sxs-lookup"><span data-stu-id="81469-133">NOTES</span></span>

## <span data-ttu-id="81469-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="81469-134">RELATED LINKS</span></span>

[<span data-ttu-id="81469-135">AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="81469-135">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="81469-136">新-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="81469-136">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="81469-137">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="81469-137">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)



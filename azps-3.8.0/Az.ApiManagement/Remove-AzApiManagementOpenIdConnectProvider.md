---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: ab278dcf56646463e1ccbc8ada9baa896b1759bf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958094"
---
# <span data-ttu-id="b74a1-101">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b74a1-101">Remove-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="b74a1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b74a1-102">SYNOPSIS</span></span>
<span data-ttu-id="b74a1-103">移除 OpenID 連接提供者。</span><span class="sxs-lookup"><span data-stu-id="b74a1-103">Removes an OpenID Connect provider.</span></span>

## <span data-ttu-id="b74a1-104">句法</span><span class="sxs-lookup"><span data-stu-id="b74a1-104">SYNTAX</span></span>

```
Remove-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b74a1-105">說明</span><span class="sxs-lookup"><span data-stu-id="b74a1-105">DESCRIPTION</span></span>
<span data-ttu-id="b74a1-106">**AzApiManagementOpenIdConnectProvider** Cmdlet 會針對 Azure API 管理移除 OpenID 連接提供者。</span><span class="sxs-lookup"><span data-stu-id="b74a1-106">The **Remove-AzApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="b74a1-107">示例</span><span class="sxs-lookup"><span data-stu-id="b74a1-107">EXAMPLES</span></span>

### <span data-ttu-id="b74a1-108">範例1：移除提供者</span><span class="sxs-lookup"><span data-stu-id="b74a1-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -PassThru
```

<span data-ttu-id="b74a1-109">這個命令會移除 ID 為 OICProvider01 的提供者。</span><span class="sxs-lookup"><span data-stu-id="b74a1-109">This command removes a provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="b74a1-110">參數</span><span class="sxs-lookup"><span data-stu-id="b74a1-110">PARAMETERS</span></span>

### <span data-ttu-id="b74a1-111">-內容</span><span class="sxs-lookup"><span data-stu-id="b74a1-111">-Context</span></span>
<span data-ttu-id="b74a1-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="b74a1-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b74a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b74a1-113">-DefaultProfile</span></span>
<span data-ttu-id="b74a1-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b74a1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b74a1-115">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="b74a1-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="b74a1-116">指定此 Cmdlet 移除之提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b74a1-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b74a1-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b74a1-117">-PassThru</span></span>
<span data-ttu-id="b74a1-118">指示這個 Cmdlet 會傳回 $True 的值（如果操作成功或 $False 則不然）。</span><span class="sxs-lookup"><span data-stu-id="b74a1-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="b74a1-119">-確認</span><span class="sxs-lookup"><span data-stu-id="b74a1-119">-Confirm</span></span>
<span data-ttu-id="b74a1-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b74a1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b74a1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b74a1-121">-WhatIf</span></span>
<span data-ttu-id="b74a1-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b74a1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b74a1-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b74a1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b74a1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b74a1-124">CommonParameters</span></span>
<span data-ttu-id="b74a1-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b74a1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b74a1-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b74a1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b74a1-127">輸入</span><span class="sxs-lookup"><span data-stu-id="b74a1-127">INPUTS</span></span>

### <span data-ttu-id="b74a1-128">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="b74a1-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b74a1-129">System.object</span><span class="sxs-lookup"><span data-stu-id="b74a1-129">System.String</span></span>

### <span data-ttu-id="b74a1-130">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="b74a1-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b74a1-131">輸出</span><span class="sxs-lookup"><span data-stu-id="b74a1-131">OUTPUTS</span></span>

### <span data-ttu-id="b74a1-132">System.object</span><span class="sxs-lookup"><span data-stu-id="b74a1-132">System.Boolean</span></span>

## <span data-ttu-id="b74a1-133">筆記</span><span class="sxs-lookup"><span data-stu-id="b74a1-133">NOTES</span></span>

## <span data-ttu-id="b74a1-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="b74a1-134">RELATED LINKS</span></span>

[<span data-ttu-id="b74a1-135">AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b74a1-135">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="b74a1-136">新-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b74a1-136">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="b74a1-137">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="b74a1-137">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)



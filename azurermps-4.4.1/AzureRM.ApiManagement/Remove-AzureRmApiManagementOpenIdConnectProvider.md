---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 686b988ef5bf62e5eed7e4f8fae94f6b29b1b4ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447192"
---
# <span data-ttu-id="a1099-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="a1099-101">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="a1099-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a1099-102">SYNOPSIS</span></span>
<span data-ttu-id="a1099-103">移除 OpenID 連接提供者。</span><span class="sxs-lookup"><span data-stu-id="a1099-103">Removes an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1099-104">句法</span><span class="sxs-lookup"><span data-stu-id="a1099-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a1099-105">說明</span><span class="sxs-lookup"><span data-stu-id="a1099-105">DESCRIPTION</span></span>
<span data-ttu-id="a1099-106">**AzureRmApiManagementOpenIdConnectProvider** Cmdlet 會針對 Azure API 管理移除 OpenID 連接提供者。</span><span class="sxs-lookup"><span data-stu-id="a1099-106">The **Remove-AzureRmApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="a1099-107">示例</span><span class="sxs-lookup"><span data-stu-id="a1099-107">EXAMPLES</span></span>

### <span data-ttu-id="a1099-108">範例1：移除提供者</span><span class="sxs-lookup"><span data-stu-id="a1099-108">Example 1: Remove a provider</span></span>
```
PS C:\>Remove-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01" -PassThru
```

<span data-ttu-id="a1099-109">這個命令會移除 ID 為 OICProvicer01 的提供者。</span><span class="sxs-lookup"><span data-stu-id="a1099-109">This command removes a provider that has the ID OICProvicer01.</span></span>

## <span data-ttu-id="a1099-110">參數</span><span class="sxs-lookup"><span data-stu-id="a1099-110">PARAMETERS</span></span>

### <span data-ttu-id="a1099-111">-內容</span><span class="sxs-lookup"><span data-stu-id="a1099-111">-Context</span></span>
<span data-ttu-id="a1099-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="a1099-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a1099-113">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="a1099-113">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="a1099-114">指定此 Cmdlet 移除之提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a1099-114">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a1099-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1099-115">-PassThru</span></span>
<span data-ttu-id="a1099-116">指示這個 Cmdlet 會傳回 $True 的值（如果操作成功或 $False 則不然）。</span><span class="sxs-lookup"><span data-stu-id="a1099-116">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="a1099-117">-確認</span><span class="sxs-lookup"><span data-stu-id="a1099-117">-Confirm</span></span>
<span data-ttu-id="a1099-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a1099-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1099-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1099-119">-WhatIf</span></span>
<span data-ttu-id="a1099-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a1099-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1099-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a1099-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1099-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1099-122">-DefaultProfile</span></span>
<span data-ttu-id="a1099-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a1099-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1099-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1099-124">CommonParameters</span></span>
<span data-ttu-id="a1099-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a1099-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1099-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a1099-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1099-127">輸入</span><span class="sxs-lookup"><span data-stu-id="a1099-127">INPUTS</span></span>

## <span data-ttu-id="a1099-128">輸出</span><span class="sxs-lookup"><span data-stu-id="a1099-128">OUTPUTS</span></span>

### <span data-ttu-id="a1099-129">布林值</span><span class="sxs-lookup"><span data-stu-id="a1099-129">Boolean</span></span>

## <span data-ttu-id="a1099-130">筆記</span><span class="sxs-lookup"><span data-stu-id="a1099-130">NOTES</span></span>

## <span data-ttu-id="a1099-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1099-131">RELATED LINKS</span></span>

[<span data-ttu-id="a1099-132">AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="a1099-132">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="a1099-133">新-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="a1099-133">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="a1099-134">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="a1099-134">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)



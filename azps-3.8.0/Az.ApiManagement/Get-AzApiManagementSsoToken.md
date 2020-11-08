---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: 25c2439c07c9fe0b611c5b845f56e1de04f4d375
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966101"
---
# <span data-ttu-id="7a631-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="7a631-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="7a631-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7a631-102">SYNOPSIS</span></span>
<span data-ttu-id="7a631-103">取得 API 管理服務之已部署管理入口網站的 SSO 標記連結。</span><span class="sxs-lookup"><span data-stu-id="7a631-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="7a631-104">句法</span><span class="sxs-lookup"><span data-stu-id="7a631-104">SYNTAX</span></span>

### <span data-ttu-id="7a631-105">ExpandedParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="7a631-105">ExpandedParameter (Default)</span></span>
```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a631-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7a631-106">ByInputObject</span></span>
```
Get-AzApiManagementSsoToken -InputObject <PsApiManagement> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a631-107">說明</span><span class="sxs-lookup"><span data-stu-id="7a631-107">DESCRIPTION</span></span>
<span data-ttu-id="7a631-108">**AzApiManagementSsoToken** Cmdlet 會傳回 (URL) 的連結，其中包含單一登入 (SSO) 權杖至 API 管理服務的部署管理入口網站。</span><span class="sxs-lookup"><span data-stu-id="7a631-108">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="7a631-109">示例</span><span class="sxs-lookup"><span data-stu-id="7a631-109">EXAMPLES</span></span>

### <span data-ttu-id="7a631-110">範例1：取得 API 管理服務的 SSO 權杖</span><span class="sxs-lookup"><span data-stu-id="7a631-110">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="7a631-111">這個命令會取得 API 管理服務的 SSO 權杖。</span><span class="sxs-lookup"><span data-stu-id="7a631-111">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="7a631-112">參數</span><span class="sxs-lookup"><span data-stu-id="7a631-112">PARAMETERS</span></span>

### <span data-ttu-id="7a631-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a631-113">-DefaultProfile</span></span>
<span data-ttu-id="7a631-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7a631-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a631-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a631-115">-InputObject</span></span>
<span data-ttu-id="7a631-116">PsApiManagement 的實例。</span><span class="sxs-lookup"><span data-stu-id="7a631-116">Instance of PsApiManagement.</span></span> <span data-ttu-id="7a631-117">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="7a631-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a631-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="7a631-118">-Name</span></span>
<span data-ttu-id="7a631-119">指定 API 管理實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="7a631-119">Specifies the name of the API Management instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a631-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a631-120">-ResourceGroupName</span></span>
<span data-ttu-id="7a631-121">指定 API 管理所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7a631-121">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a631-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a631-122">CommonParameters</span></span>
<span data-ttu-id="7a631-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7a631-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a631-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7a631-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a631-125">輸入</span><span class="sxs-lookup"><span data-stu-id="7a631-125">INPUTS</span></span>

### <span data-ttu-id="7a631-126">System.object</span><span class="sxs-lookup"><span data-stu-id="7a631-126">System.String</span></span>

## <span data-ttu-id="7a631-127">輸出</span><span class="sxs-lookup"><span data-stu-id="7a631-127">OUTPUTS</span></span>

### <span data-ttu-id="7a631-128">System.object</span><span class="sxs-lookup"><span data-stu-id="7a631-128">System.String</span></span>

## <span data-ttu-id="7a631-129">筆記</span><span class="sxs-lookup"><span data-stu-id="7a631-129">NOTES</span></span>

## <span data-ttu-id="7a631-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="7a631-130">RELATED LINKS</span></span>

[<span data-ttu-id="7a631-131">AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="7a631-131">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: eae199f28314db5aa50fa3247b46f02a407802fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915693"
---
# <span data-ttu-id="94e4b-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="94e4b-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="94e4b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="94e4b-102">SYNOPSIS</span></span>
<span data-ttu-id="94e4b-103">使用 SSO 權杖連結至 API 管理服務的部署管理入口網站。</span><span class="sxs-lookup"><span data-stu-id="94e4b-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="94e4b-104">語法</span><span class="sxs-lookup"><span data-stu-id="94e4b-104">SYNTAX</span></span>

### <span data-ttu-id="94e4b-105">展開Parameter (預設) </span><span class="sxs-lookup"><span data-stu-id="94e4b-105">ExpandedParameter (Default)</span></span>
```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94e4b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="94e4b-106">ByInputObject</span></span>
```
Get-AzApiManagementSsoToken -InputObject <PsApiManagement> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94e4b-107">描述</span><span class="sxs-lookup"><span data-stu-id="94e4b-107">DESCRIPTION</span></span>
<span data-ttu-id="94e4b-108">**Get-AzApiManagementSsoToken Cmdlet** 會傳送連結 (URL) ，其中包含單一登入 (SSO) 權杖至 API 管理服務的部署管理入口網站。</span><span class="sxs-lookup"><span data-stu-id="94e4b-108">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="94e4b-109">例子</span><span class="sxs-lookup"><span data-stu-id="94e4b-109">EXAMPLES</span></span>

### <span data-ttu-id="94e4b-110">範例 1：取得 API 管理服務的 SSO 權杖</span><span class="sxs-lookup"><span data-stu-id="94e4b-110">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="94e4b-111">此命令會獲得 API 管理服務的 SSO 權杖。</span><span class="sxs-lookup"><span data-stu-id="94e4b-111">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="94e4b-112">參數</span><span class="sxs-lookup"><span data-stu-id="94e4b-112">PARAMETERS</span></span>

### <span data-ttu-id="94e4b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94e4b-113">-DefaultProfile</span></span>
<span data-ttu-id="94e4b-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="94e4b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94e4b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94e4b-115">-InputObject</span></span>
<span data-ttu-id="94e4b-116">PsApiManagement 實例。</span><span class="sxs-lookup"><span data-stu-id="94e4b-116">Instance of PsApiManagement.</span></span> <span data-ttu-id="94e4b-117">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="94e4b-117">This parameter is required.</span></span>

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

### <span data-ttu-id="94e4b-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="94e4b-118">-Name</span></span>
<span data-ttu-id="94e4b-119">指定 API 管理實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="94e4b-119">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="94e4b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94e4b-120">-ResourceGroupName</span></span>
<span data-ttu-id="94e4b-121">指定 API 管理存在之資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="94e4b-121">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="94e4b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94e4b-122">CommonParameters</span></span>
<span data-ttu-id="94e4b-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="94e4b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94e4b-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94e4b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94e4b-125">輸入</span><span class="sxs-lookup"><span data-stu-id="94e4b-125">INPUTS</span></span>

### <span data-ttu-id="94e4b-126">System.String</span><span class="sxs-lookup"><span data-stu-id="94e4b-126">System.String</span></span>

## <span data-ttu-id="94e4b-127">輸出</span><span class="sxs-lookup"><span data-stu-id="94e4b-127">OUTPUTS</span></span>

### <span data-ttu-id="94e4b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="94e4b-128">System.String</span></span>

## <span data-ttu-id="94e4b-129">筆記</span><span class="sxs-lookup"><span data-stu-id="94e4b-129">NOTES</span></span>

## <span data-ttu-id="94e4b-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="94e4b-130">RELATED LINKS</span></span>

[<span data-ttu-id="94e4b-131">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="94e4b-131">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)



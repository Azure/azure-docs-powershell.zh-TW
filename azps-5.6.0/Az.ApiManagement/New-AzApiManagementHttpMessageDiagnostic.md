---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementhttpmessagediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
ms.openlocfilehash: 3475778104655e6b27061edf08ced376f192ea34
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911206"
---
# <span data-ttu-id="61e01-101">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="61e01-101">New-AzApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="61e01-102">簡介</span><span class="sxs-lookup"><span data-stu-id="61e01-102">SYNOPSIS</span></span>
<span data-ttu-id="61e01-103">建立 **PsApiManagementHttpMessageDiagnostic** 的實例，此為診斷的 Http 訊息診斷設定</span><span class="sxs-lookup"><span data-stu-id="61e01-103">Creates an instance of **PsApiManagementHttpMessageDiagnostic** which is an Http Message diagnostic setting of the Diagnostic</span></span>

## <span data-ttu-id="61e01-104">語法</span><span class="sxs-lookup"><span data-stu-id="61e01-104">SYNTAX</span></span>

```
New-AzApiManagementHttpMessageDiagnostic [-HeadersToLog <String[]>] [-BodyBytesToLog <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61e01-105">描述</span><span class="sxs-lookup"><span data-stu-id="61e01-105">DESCRIPTION</span></span>
<span data-ttu-id="61e01-106">Cmdlet **New-AzApiManagementHttpMessageDiagnostic** 會建立 HTTP Message 診斷設定。</span><span class="sxs-lookup"><span data-stu-id="61e01-106">The cmdlet **New-AzApiManagementHttpMessageDiagnostic** creates the Http Message diagnostic setting.</span></span>

## <span data-ttu-id="61e01-107">例子</span><span class="sxs-lookup"><span data-stu-id="61e01-107">EXAMPLES</span></span>

### <span data-ttu-id="61e01-108">範例 1：建立基本 Http 訊息診斷設定</span><span class="sxs-lookup"><span data-stu-id="61e01-108">Example 1: Create a Basic Http Message diagnostic Setting</span></span>
```powershell
PS C:\>  New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100

Headers                   Body
-------                   ----
{Content-Type, UserAgent} Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBodyDiagnosticSetting
```

<span data-ttu-id="61e01-109">建立 HTTP 訊息診斷設定以記錄及標題，以及 `Content-Type` `User-Agent` 100 位元組的 `body`</span><span class="sxs-lookup"><span data-stu-id="61e01-109">Create a http message diagnostic setting to log `Content-Type` and `User-Agent` headers along with 100 bytes of `body`</span></span>

## <span data-ttu-id="61e01-110">參數</span><span class="sxs-lookup"><span data-stu-id="61e01-110">PARAMETERS</span></span>

### <span data-ttu-id="61e01-111">-BodyBytesToLog</span><span class="sxs-lookup"><span data-stu-id="61e01-111">-BodyBytesToLog</span></span>
<span data-ttu-id="61e01-112">要記錄的要求內位元組數。</span><span class="sxs-lookup"><span data-stu-id="61e01-112">Number of request body bytes to log.</span></span> <span data-ttu-id="61e01-113">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="61e01-113">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e01-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61e01-114">-DefaultProfile</span></span>
<span data-ttu-id="61e01-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="61e01-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61e01-116">-HeadersToLog</span><span class="sxs-lookup"><span data-stu-id="61e01-116">-HeadersToLog</span></span>
<span data-ttu-id="61e01-117">要記錄的標題陣列。</span><span class="sxs-lookup"><span data-stu-id="61e01-117">The array of headers to log.</span></span> <span data-ttu-id="61e01-118">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="61e01-118">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e01-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61e01-119">CommonParameters</span></span>
<span data-ttu-id="61e01-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="61e01-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61e01-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61e01-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61e01-122">輸入</span><span class="sxs-lookup"><span data-stu-id="61e01-122">INPUTS</span></span>

### <span data-ttu-id="61e01-123">沒有</span><span class="sxs-lookup"><span data-stu-id="61e01-123">None</span></span>

## <span data-ttu-id="61e01-124">輸出</span><span class="sxs-lookup"><span data-stu-id="61e01-124">OUTPUTS</span></span>

### <span data-ttu-id="61e01-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="61e01-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="61e01-126">筆記</span><span class="sxs-lookup"><span data-stu-id="61e01-126">NOTES</span></span>

## <span data-ttu-id="61e01-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="61e01-127">RELATED LINKS</span></span>

[<span data-ttu-id="61e01-128">New-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="61e01-128">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="61e01-129">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="61e01-129">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)
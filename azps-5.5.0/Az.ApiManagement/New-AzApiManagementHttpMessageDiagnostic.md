---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementhttpmessagediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
ms.openlocfilehash: 10c84654bb5d074ee9f668062d1fa7a18d92f8b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139670"
---
# <span data-ttu-id="83304-101">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="83304-101">New-AzApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="83304-102">摘要</span><span class="sxs-lookup"><span data-stu-id="83304-102">SYNOPSIS</span></span>
<span data-ttu-id="83304-103">建立 **PsApiManagementHttpMessageDiagnostic** 的實例，這是診斷的 Http 郵件診斷設定</span><span class="sxs-lookup"><span data-stu-id="83304-103">Creates an instance of **PsApiManagementHttpMessageDiagnostic** which is an Http Message diagnostic setting of the Diagnostic</span></span>

## <span data-ttu-id="83304-104">句法</span><span class="sxs-lookup"><span data-stu-id="83304-104">SYNTAX</span></span>

```
New-AzApiManagementHttpMessageDiagnostic [-HeadersToLog <String[]>] [-BodyBytesToLog <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83304-105">說明</span><span class="sxs-lookup"><span data-stu-id="83304-105">DESCRIPTION</span></span>
<span data-ttu-id="83304-106">Cmdlet **AzApiManagementHttpMessageDiagnostic** 會建立 Http 訊息診斷設定。</span><span class="sxs-lookup"><span data-stu-id="83304-106">The cmdlet **New-AzApiManagementHttpMessageDiagnostic** creates the Http Message diagnostic setting.</span></span>

## <span data-ttu-id="83304-107">示例</span><span class="sxs-lookup"><span data-stu-id="83304-107">EXAMPLES</span></span>

### <span data-ttu-id="83304-108">範例1：建立基本 Http 郵件診斷設定</span><span class="sxs-lookup"><span data-stu-id="83304-108">Example 1: Create a Basic Http Message diagnostic Setting</span></span>
```powershell
PS C:\>  New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100

Headers                   Body
-------                   ----
{Content-Type, UserAgent} Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBodyDiagnosticSetting
```

<span data-ttu-id="83304-109">在記錄和標頭中建立 HTTP 郵件診斷設定， `Content-Type` 並將 `User-Agent` 100 個位元組結合 `body`</span><span class="sxs-lookup"><span data-stu-id="83304-109">Create a http message diagnostic setting to log `Content-Type` and `User-Agent` headers along with 100 bytes of `body`</span></span>

## <span data-ttu-id="83304-110">參數</span><span class="sxs-lookup"><span data-stu-id="83304-110">PARAMETERS</span></span>

### <span data-ttu-id="83304-111">-BodyBytesToLog</span><span class="sxs-lookup"><span data-stu-id="83304-111">-BodyBytesToLog</span></span>
<span data-ttu-id="83304-112">要記錄的要求主體位元組數。</span><span class="sxs-lookup"><span data-stu-id="83304-112">Number of request body bytes to log.</span></span> <span data-ttu-id="83304-113">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="83304-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="83304-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83304-114">-DefaultProfile</span></span>
<span data-ttu-id="83304-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="83304-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83304-116">-HeadersToLog</span><span class="sxs-lookup"><span data-stu-id="83304-116">-HeadersToLog</span></span>
<span data-ttu-id="83304-117">要記錄的標頭陣列。</span><span class="sxs-lookup"><span data-stu-id="83304-117">The array of headers to log.</span></span> <span data-ttu-id="83304-118">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="83304-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="83304-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83304-119">CommonParameters</span></span>
<span data-ttu-id="83304-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="83304-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83304-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="83304-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83304-122">輸入</span><span class="sxs-lookup"><span data-stu-id="83304-122">INPUTS</span></span>

### <span data-ttu-id="83304-123">所有</span><span class="sxs-lookup"><span data-stu-id="83304-123">None</span></span>

## <span data-ttu-id="83304-124">輸出</span><span class="sxs-lookup"><span data-stu-id="83304-124">OUTPUTS</span></span>

### <span data-ttu-id="83304-125">ServiceManagement. PsApiManagementHttpMessageDiagnostic （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="83304-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="83304-126">筆記</span><span class="sxs-lookup"><span data-stu-id="83304-126">NOTES</span></span>

## <span data-ttu-id="83304-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="83304-127">RELATED LINKS</span></span>

[<span data-ttu-id="83304-128">新-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="83304-128">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="83304-129">新-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="83304-129">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)
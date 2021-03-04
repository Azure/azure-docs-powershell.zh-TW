---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementpipelinediagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
ms.openlocfilehash: e68449a84bb64454291434bded40ed2e494fdab4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908685"
---
# <span data-ttu-id="15fd6-101">New-AzApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="15fd6-101">New-AzApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="15fd6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="15fd6-102">SYNOPSIS</span></span>
<span data-ttu-id="15fd6-103">為傳入/傳出的 HTTP 郵件建立閘道的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="15fd6-103">Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="15fd6-104">語法</span><span class="sxs-lookup"><span data-stu-id="15fd6-104">SYNTAX</span></span>

```
New-AzApiManagementPipelineDiagnosticSetting [-Request <PsApiManagementHttpMessageDiagnostic>]
 [-Response <PsApiManagementHttpMessageDiagnostic>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15fd6-105">描述</span><span class="sxs-lookup"><span data-stu-id="15fd6-105">DESCRIPTION</span></span>
<span data-ttu-id="15fd6-106">Cmdlet **New-AzApiManagementPipelineDiagnosticSetting** 會針對傳入/外寄的 HTTP 郵件建立閘道的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="15fd6-106">The cmdlet **New-AzApiManagementPipelineDiagnosticSetting** creates the Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="15fd6-107">例子</span><span class="sxs-lookup"><span data-stu-id="15fd6-107">EXAMPLES</span></span>

### <span data-ttu-id="15fd6-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="15fd6-108">Example 1</span></span>
```powershell
PS c:\> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100
PS c:\> New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic

Request                                                                                              Response
-------                                                                                              --------
Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
```

<span data-ttu-id="15fd6-109">建立管線診斷，以用於診斷實體的 FrontEnd 或後端。</span><span class="sxs-lookup"><span data-stu-id="15fd6-109">Create a pipeline diagnostic to be used in either FrontEnd or Backend in the Diagnostic Entity.</span></span>

## <span data-ttu-id="15fd6-110">參數</span><span class="sxs-lookup"><span data-stu-id="15fd6-110">PARAMETERS</span></span>

### <span data-ttu-id="15fd6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15fd6-111">-DefaultProfile</span></span>
<span data-ttu-id="15fd6-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="15fd6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15fd6-113">-要求</span><span class="sxs-lookup"><span data-stu-id="15fd6-113">-Request</span></span>
<span data-ttu-id="15fd6-114">要求診斷設定。</span><span class="sxs-lookup"><span data-stu-id="15fd6-114">Diagnostic setting for Request.</span></span>
<span data-ttu-id="15fd6-115">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="15fd6-115">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15fd6-116">-回復</span><span class="sxs-lookup"><span data-stu-id="15fd6-116">-Response</span></span>
<span data-ttu-id="15fd6-117">回應的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="15fd6-117">Diagnostic setting for Response.</span></span>
<span data-ttu-id="15fd6-118">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="15fd6-118">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15fd6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15fd6-119">CommonParameters</span></span>
<span data-ttu-id="15fd6-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="15fd6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15fd6-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15fd6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15fd6-122">輸入</span><span class="sxs-lookup"><span data-stu-id="15fd6-122">INPUTS</span></span>

### <span data-ttu-id="15fd6-123">沒有</span><span class="sxs-lookup"><span data-stu-id="15fd6-123">None</span></span>

## <span data-ttu-id="15fd6-124">輸出</span><span class="sxs-lookup"><span data-stu-id="15fd6-124">OUTPUTS</span></span>

### <span data-ttu-id="15fd6-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="15fd6-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="15fd6-126">筆記</span><span class="sxs-lookup"><span data-stu-id="15fd6-126">NOTES</span></span>

## <span data-ttu-id="15fd6-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="15fd6-127">RELATED LINKS</span></span>

[<span data-ttu-id="15fd6-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="15fd6-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="15fd6-129">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="15fd6-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="15fd6-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="15fd6-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="15fd6-131">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="15fd6-131">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)



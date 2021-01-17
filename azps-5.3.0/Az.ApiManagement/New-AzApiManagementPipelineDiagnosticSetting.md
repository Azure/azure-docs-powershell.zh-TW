---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementpipelinediagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
ms.openlocfilehash: 7e6f6515b24a7cefabd40a6fdfaedfda430f69d0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98287852"
---
# <span data-ttu-id="27cfc-101">New-AzApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="27cfc-101">New-AzApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="27cfc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="27cfc-102">SYNOPSIS</span></span>
<span data-ttu-id="27cfc-103">建立傳入/傳出 HTTP 訊息的診斷設定至閘道。</span><span class="sxs-lookup"><span data-stu-id="27cfc-103">Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="27cfc-104">句法</span><span class="sxs-lookup"><span data-stu-id="27cfc-104">SYNTAX</span></span>

```
New-AzApiManagementPipelineDiagnosticSetting [-Request <PsApiManagementHttpMessageDiagnostic>]
 [-Response <PsApiManagementHttpMessageDiagnostic>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="27cfc-105">說明</span><span class="sxs-lookup"><span data-stu-id="27cfc-105">DESCRIPTION</span></span>
<span data-ttu-id="27cfc-106">Cmdlet **AzApiManagementPipelineDiagnosticSetting** 會建立傳入/傳出 HTTP 訊息的診斷設定至閘道。</span><span class="sxs-lookup"><span data-stu-id="27cfc-106">The cmdlet **New-AzApiManagementPipelineDiagnosticSetting** creates the Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="27cfc-107">示例</span><span class="sxs-lookup"><span data-stu-id="27cfc-107">EXAMPLES</span></span>

### <span data-ttu-id="27cfc-108">範例1</span><span class="sxs-lookup"><span data-stu-id="27cfc-108">Example 1</span></span>
```powershell
PS c:\> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100
PS c:\> New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic

Request                                                                                              Response
-------                                                                                              --------
Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
```

<span data-ttu-id="27cfc-109">建立要用於診斷實體中前端或後端的管線診斷程式。</span><span class="sxs-lookup"><span data-stu-id="27cfc-109">Create a pipeline diagnostic to be used in either FrontEnd or Backend in the Diagnostic Entity.</span></span>

## <span data-ttu-id="27cfc-110">參數</span><span class="sxs-lookup"><span data-stu-id="27cfc-110">PARAMETERS</span></span>

### <span data-ttu-id="27cfc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27cfc-111">-DefaultProfile</span></span>
<span data-ttu-id="27cfc-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="27cfc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27cfc-113">-要求</span><span class="sxs-lookup"><span data-stu-id="27cfc-113">-Request</span></span>
<span data-ttu-id="27cfc-114">要求的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="27cfc-114">Diagnostic setting for Request.</span></span>
<span data-ttu-id="27cfc-115">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="27cfc-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="27cfc-116">-回應</span><span class="sxs-lookup"><span data-stu-id="27cfc-116">-Response</span></span>
<span data-ttu-id="27cfc-117">[回應] 的診斷設定。</span><span class="sxs-lookup"><span data-stu-id="27cfc-117">Diagnostic setting for Response.</span></span>
<span data-ttu-id="27cfc-118">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="27cfc-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="27cfc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27cfc-119">CommonParameters</span></span>
<span data-ttu-id="27cfc-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="27cfc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27cfc-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="27cfc-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27cfc-122">輸入</span><span class="sxs-lookup"><span data-stu-id="27cfc-122">INPUTS</span></span>

### <span data-ttu-id="27cfc-123">所有</span><span class="sxs-lookup"><span data-stu-id="27cfc-123">None</span></span>

## <span data-ttu-id="27cfc-124">輸出</span><span class="sxs-lookup"><span data-stu-id="27cfc-124">OUTPUTS</span></span>

### <span data-ttu-id="27cfc-125">ServiceManagement. PsApiManagementPipelineDiagnosticSetting （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="27cfc-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="27cfc-126">筆記</span><span class="sxs-lookup"><span data-stu-id="27cfc-126">NOTES</span></span>

## <span data-ttu-id="27cfc-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="27cfc-127">RELATED LINKS</span></span>

[<span data-ttu-id="27cfc-128">AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="27cfc-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="27cfc-129">移除-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="27cfc-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="27cfc-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="27cfc-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="27cfc-131">新-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="27cfc-131">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsamplingsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSamplingSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSamplingSetting.md
ms.openlocfilehash: 61f046576c14b61a59b55c52dd69c3e72b2c839e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958159"
---
# <span data-ttu-id="8df87-101">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="8df87-101">New-AzApiManagementSamplingSetting</span></span>

## <span data-ttu-id="8df87-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8df87-102">SYNOPSIS</span></span>
<span data-ttu-id="8df87-103">為診斷建立新的採樣設定</span><span class="sxs-lookup"><span data-stu-id="8df87-103">Create a new sampling setting for the Diagnostic</span></span>

## <span data-ttu-id="8df87-104">句法</span><span class="sxs-lookup"><span data-stu-id="8df87-104">SYNTAX</span></span>

```
New-AzApiManagementSamplingSetting [-SamplingType <String>] [-SamplingPercentage <Double>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8df87-105">說明</span><span class="sxs-lookup"><span data-stu-id="8df87-105">DESCRIPTION</span></span>
<span data-ttu-id="8df87-106">Cmdlet [ **New-AzApiManagementSamplingSetting** ] 會為診斷程式建立新的採樣設定</span><span class="sxs-lookup"><span data-stu-id="8df87-106">The cmdlet **New-AzApiManagementSamplingSetting** creates a new sampling setting for the Diagnostic</span></span>

## <span data-ttu-id="8df87-107">示例</span><span class="sxs-lookup"><span data-stu-id="8df87-107">EXAMPLES</span></span>

### <span data-ttu-id="8df87-108">範例1：建立基本的採樣設定</span><span class="sxs-lookup"><span data-stu-id="8df87-108">Example 1 : Create a basic Sampling setting</span></span>
```powershell
PS C:\> New-AzApiManagementSamplingSetting -SamplingType fixed -Percentage 100

SamplingType Percentage
------------ ----------
fixed               100
```

<span data-ttu-id="8df87-109">`Fixed`使用100% 的要求/回應的記錄來建立類型的採樣設定</span><span class="sxs-lookup"><span data-stu-id="8df87-109">Creates a sampling setting of `Fixed` type with logging for 100% of the requests / responses</span></span>

## <span data-ttu-id="8df87-110">參數</span><span class="sxs-lookup"><span data-stu-id="8df87-110">PARAMETERS</span></span>

### <span data-ttu-id="8df87-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8df87-111">-DefaultProfile</span></span>
<span data-ttu-id="8df87-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8df87-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8df87-113">-SamplingPercentage</span><span class="sxs-lookup"><span data-stu-id="8df87-113">-SamplingPercentage</span></span>
<span data-ttu-id="8df87-114">固定比率採樣採樣的速率。</span><span class="sxs-lookup"><span data-stu-id="8df87-114">Rate of Sampling for Fixed Rate Sampling.</span></span> <span data-ttu-id="8df87-115">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="8df87-115">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8df87-116">-SamplingType</span><span class="sxs-lookup"><span data-stu-id="8df87-116">-SamplingType</span></span>
<span data-ttu-id="8df87-117">取樣類型。</span><span class="sxs-lookup"><span data-stu-id="8df87-117">The Type of Sampling.</span></span>
<span data-ttu-id="8df87-118">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="8df87-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8df87-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8df87-119">CommonParameters</span></span>
<span data-ttu-id="8df87-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8df87-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8df87-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8df87-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8df87-122">輸入</span><span class="sxs-lookup"><span data-stu-id="8df87-122">INPUTS</span></span>

### <span data-ttu-id="8df87-123">所有</span><span class="sxs-lookup"><span data-stu-id="8df87-123">None</span></span>

## <span data-ttu-id="8df87-124">輸出</span><span class="sxs-lookup"><span data-stu-id="8df87-124">OUTPUTS</span></span>

### <span data-ttu-id="8df87-125">ServiceManagement. PsApiManagementSamplingSetting （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="8df87-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

## <span data-ttu-id="8df87-126">筆記</span><span class="sxs-lookup"><span data-stu-id="8df87-126">NOTES</span></span>

## <span data-ttu-id="8df87-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="8df87-127">RELATED LINKS</span></span>

[<span data-ttu-id="8df87-128">AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8df87-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="8df87-129">移除-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8df87-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="8df87-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="8df87-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="8df87-131">新-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="8df87-131">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)

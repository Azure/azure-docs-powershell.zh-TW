---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 5fcd81dcfc69f020a4e17e0858abfca0edaba405
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907178"
---
# <span data-ttu-id="3f5e3-101">Get-AzAccessToken</span><span class="sxs-lookup"><span data-stu-id="3f5e3-101">Get-AzAccessToken</span></span>

## <span data-ttu-id="3f5e3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3f5e3-102">SYNOPSIS</span></span>
<span data-ttu-id="3f5e3-103">取得原始存取權杖。</span><span class="sxs-lookup"><span data-stu-id="3f5e3-103">Get raw access token.</span></span> <span data-ttu-id="3f5e3-104">使用 -ResourceUrl 時，請確定該值與目前的 Azure 環境相符。</span><span class="sxs-lookup"><span data-stu-id="3f5e3-104">When using -ResourceUrl, please make sure the value does match current Azure environment.</span></span> <span data-ttu-id="3f5e3-105">您可以參照到 的值 `(Get-AzContext).Environment` 。</span><span class="sxs-lookup"><span data-stu-id="3f5e3-105">You may refer to the value of `(Get-AzContext).Environment`.</span></span>

## <span data-ttu-id="3f5e3-106">語法</span><span class="sxs-lookup"><span data-stu-id="3f5e3-106">SYNTAX</span></span>

### <span data-ttu-id="3f5e3-107">KnownResourceTypeName (預設) </span><span class="sxs-lookup"><span data-stu-id="3f5e3-107">KnownResourceTypeName (Default)</span></span>
```
Get-AzAccessToken [-ResourceTypeName <String>] [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f5e3-108">ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="3f5e3-108">ResourceUrl</span></span>
```
Get-AzAccessToken -ResourceUrl <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f5e3-109">描述</span><span class="sxs-lookup"><span data-stu-id="3f5e3-109">DESCRIPTION</span></span>
<span data-ttu-id="3f5e3-110">取得存取權杖</span><span class="sxs-lookup"><span data-stu-id="3f5e3-110">Get access token</span></span>

## <span data-ttu-id="3f5e3-111">例子</span><span class="sxs-lookup"><span data-stu-id="3f5e3-111">EXAMPLES</span></span>

### <span data-ttu-id="3f5e3-112">範例 1 取得 ARM 端點的原始存取權杖</span><span class="sxs-lookup"><span data-stu-id="3f5e3-112">Example 1 Get raw access token for ARM endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken
```

<span data-ttu-id="3f5e3-113">取得目前帳戶 ResourceManager 端點的存取權杖</span><span class="sxs-lookup"><span data-stu-id="3f5e3-113">Get access token of ResourceManager endpoint for current account</span></span>

### <span data-ttu-id="3f5e3-114">範例 2 取得 AAD 圖形端點的原始存取權杖</span><span class="sxs-lookup"><span data-stu-id="3f5e3-114">Example 2 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

<span data-ttu-id="3f5e3-115">取得目前帳戶 AAD 圖形端點的存取權杖</span><span class="sxs-lookup"><span data-stu-id="3f5e3-115">Get access token of AAD graph endpoint for current account</span></span>

### <span data-ttu-id="3f5e3-116">範例 3 取得 AAD 圖形端點的原始存取權杖</span><span class="sxs-lookup"><span data-stu-id="3f5e3-116">Example 3 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

<span data-ttu-id="3f5e3-117">取得目前帳戶 AAD 圖形端點的存取權杖</span><span class="sxs-lookup"><span data-stu-id="3f5e3-117">Get access token of AAD graph endpoint for current account</span></span>

## <span data-ttu-id="3f5e3-118">參數</span><span class="sxs-lookup"><span data-stu-id="3f5e3-118">PARAMETERS</span></span>

### <span data-ttu-id="3f5e3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f5e3-119">-DefaultProfile</span></span>
<span data-ttu-id="3f5e3-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3f5e3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f5e3-121">-ResourceTypeName</span><span class="sxs-lookup"><span data-stu-id="3f5e3-121">-ResourceTypeName</span></span>
<span data-ttu-id="3f5e3-122">選擇性的重新配置類型名稱，支援的值：AadGraph、AnalysisServices、Arm、表示、Batch、DataLake、KeyVault、OperationalInsights、ResourceManager、Synapse。</span><span class="sxs-lookup"><span data-stu-id="3f5e3-122">Optional resouce type name, supported values: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse.</span></span> <span data-ttu-id="3f5e3-123">如果沒有指定，預設值為 Arm。</span><span class="sxs-lookup"><span data-stu-id="3f5e3-123">Default value is Arm if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: KnownResourceTypeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f5e3-124">-ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="3f5e3-124">-ResourceUrl</span></span>
<span data-ttu-id="3f5e3-125">您要求權杖的資源 URL，例如' http://graph.windows.net/ '。</span><span class="sxs-lookup"><span data-stu-id="3f5e3-125">Resource url for that you're requesting token, e.g. 'http://graph.windows.net/'.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUrl
Aliases: Resource, ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f5e3-126">-TenantId</span><span class="sxs-lookup"><span data-stu-id="3f5e3-126">-TenantId</span></span>
<span data-ttu-id="3f5e3-127">選擇性的租使用者識別碼。如果未指定，請使用預設上下文的租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="3f5e3-127">Optional Tenant Id. Use tenant id of default context if not specified.</span></span>

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

### <span data-ttu-id="3f5e3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f5e3-128">CommonParameters</span></span>
<span data-ttu-id="3f5e3-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3f5e3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f5e3-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f5e3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f5e3-131">輸入</span><span class="sxs-lookup"><span data-stu-id="3f5e3-131">INPUTS</span></span>

### <span data-ttu-id="3f5e3-132">沒有</span><span class="sxs-lookup"><span data-stu-id="3f5e3-132">None</span></span>

## <span data-ttu-id="3f5e3-133">輸出</span><span class="sxs-lookup"><span data-stu-id="3f5e3-133">OUTPUTS</span></span>

### <span data-ttu-id="3f5e3-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3f5e3-134">System.String</span></span>

## <span data-ttu-id="3f5e3-135">筆記</span><span class="sxs-lookup"><span data-stu-id="3f5e3-135">NOTES</span></span>

## <span data-ttu-id="3f5e3-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="3f5e3-136">RELATED LINKS</span></span>

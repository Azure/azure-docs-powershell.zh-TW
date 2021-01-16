---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 696ae59cb5115181605b7e6e647e2eb7d2792fd8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276287"
---
# <span data-ttu-id="19d02-101">Get-AzAccessToken</span><span class="sxs-lookup"><span data-stu-id="19d02-101">Get-AzAccessToken</span></span>

## <span data-ttu-id="19d02-102">摘要</span><span class="sxs-lookup"><span data-stu-id="19d02-102">SYNOPSIS</span></span>
<span data-ttu-id="19d02-103">取得原始存取權杖。</span><span class="sxs-lookup"><span data-stu-id="19d02-103">Get raw access token.</span></span> <span data-ttu-id="19d02-104">使用-ResourceUrl 時，請確定該值與目前的 Azure 環境相符。</span><span class="sxs-lookup"><span data-stu-id="19d02-104">When using -ResourceUrl, please make sure the value does match current Azure environment.</span></span> <span data-ttu-id="19d02-105">您可能會參照的值 `(Get-AzContext).Environment` 。</span><span class="sxs-lookup"><span data-stu-id="19d02-105">You may refer to the value of `(Get-AzContext).Environment`.</span></span>

## <span data-ttu-id="19d02-106">句法</span><span class="sxs-lookup"><span data-stu-id="19d02-106">SYNTAX</span></span>

### <span data-ttu-id="19d02-107">KnownResourceTypeName (預設) </span><span class="sxs-lookup"><span data-stu-id="19d02-107">KnownResourceTypeName (Default)</span></span>
```
Get-AzAccessToken [-ResourceTypeName <String>] [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="19d02-108">ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="19d02-108">ResourceUrl</span></span>
```
Get-AzAccessToken -ResourceUrl <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="19d02-109">說明</span><span class="sxs-lookup"><span data-stu-id="19d02-109">DESCRIPTION</span></span>
<span data-ttu-id="19d02-110">取得存取權杖</span><span class="sxs-lookup"><span data-stu-id="19d02-110">Get access token</span></span>

## <span data-ttu-id="19d02-111">示例</span><span class="sxs-lookup"><span data-stu-id="19d02-111">EXAMPLES</span></span>

### <span data-ttu-id="19d02-112">範例1取得 ARM 端點的原始存取權杖</span><span class="sxs-lookup"><span data-stu-id="19d02-112">Example 1 Get raw access token for ARM endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken
```

<span data-ttu-id="19d02-113">取得目前帳戶的 ResourceManager 端點的存取權杖</span><span class="sxs-lookup"><span data-stu-id="19d02-113">Get access token of ResourceManager endpoint for current account</span></span>

### <span data-ttu-id="19d02-114">範例2取得 AAD 圖形端點的原始存取權杖</span><span class="sxs-lookup"><span data-stu-id="19d02-114">Example 2 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

<span data-ttu-id="19d02-115">取得目前帳戶的 AAD 圖形端點的存取權杖</span><span class="sxs-lookup"><span data-stu-id="19d02-115">Get access token of AAD graph endpoint for current account</span></span>

### <span data-ttu-id="19d02-116">範例3取得 AAD 圖形端點的原始存取權杖</span><span class="sxs-lookup"><span data-stu-id="19d02-116">Example 3 Get raw access token for AAD graph endpoint</span></span>
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

<span data-ttu-id="19d02-117">取得目前帳戶的 AAD 圖形端點的存取權杖</span><span class="sxs-lookup"><span data-stu-id="19d02-117">Get access token of AAD graph endpoint for current account</span></span>

## <span data-ttu-id="19d02-118">參數</span><span class="sxs-lookup"><span data-stu-id="19d02-118">PARAMETERS</span></span>

### <span data-ttu-id="19d02-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19d02-119">-DefaultProfile</span></span>
<span data-ttu-id="19d02-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="19d02-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19d02-121">-ResourceTypeName</span><span class="sxs-lookup"><span data-stu-id="19d02-121">-ResourceTypeName</span></span>
<span data-ttu-id="19d02-122">選用的資源類型名稱、支援的值： AadGraph、AnalysisServices、Arm、證明、Batch、DataLake、KeyVault、OperationalInsights、ResourceManager、Synapse。</span><span class="sxs-lookup"><span data-stu-id="19d02-122">Optional resouce type name, supported values: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse.</span></span> <span data-ttu-id="19d02-123">如果沒有指定，則預設值為 Arm。</span><span class="sxs-lookup"><span data-stu-id="19d02-123">Default value is Arm if not specified.</span></span>

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

### <span data-ttu-id="19d02-124">-ResourceUrl</span><span class="sxs-lookup"><span data-stu-id="19d02-124">-ResourceUrl</span></span>
<span data-ttu-id="19d02-125">您正在要求權杖的資源 url，例如 " http://graph.windows.net/ "。</span><span class="sxs-lookup"><span data-stu-id="19d02-125">Resource url for that you're requesting token, e.g. 'http://graph.windows.net/'.</span></span>

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

### <span data-ttu-id="19d02-126">-TenantId</span><span class="sxs-lookup"><span data-stu-id="19d02-126">-TenantId</span></span>
<span data-ttu-id="19d02-127">選用的租使用者識別碼。如果未指定，請使用預設內容的租使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="19d02-127">Optional Tenant Id. Use tenant id of default context if not specified.</span></span>

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

### <span data-ttu-id="19d02-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19d02-128">CommonParameters</span></span>
<span data-ttu-id="19d02-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="19d02-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19d02-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="19d02-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19d02-131">輸入</span><span class="sxs-lookup"><span data-stu-id="19d02-131">INPUTS</span></span>

### <span data-ttu-id="19d02-132">所有</span><span class="sxs-lookup"><span data-stu-id="19d02-132">None</span></span>

## <span data-ttu-id="19d02-133">輸出</span><span class="sxs-lookup"><span data-stu-id="19d02-133">OUTPUTS</span></span>

### <span data-ttu-id="19d02-134">System.object</span><span class="sxs-lookup"><span data-stu-id="19d02-134">System.String</span></span>

## <span data-ttu-id="19d02-135">筆記</span><span class="sxs-lookup"><span data-stu-id="19d02-135">NOTES</span></span>

## <span data-ttu-id="19d02-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="19d02-136">RELATED LINKS</span></span>

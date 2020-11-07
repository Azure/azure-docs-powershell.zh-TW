---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
ms.openlocfilehash: c5276ddbcd10870355f8530c2f04f81122dda382
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624141"
---
# <span data-ttu-id="8b273-101">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="8b273-101">Get-AzureRmADApplication</span></span>

## <span data-ttu-id="8b273-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8b273-102">SYNOPSIS</span></span>
<span data-ttu-id="8b273-103">列出現有的 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="8b273-103">Lists existing azure active directory applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b273-104">句法</span><span class="sxs-lookup"><span data-stu-id="8b273-104">SYNTAX</span></span>

### <span data-ttu-id="8b273-105">EmptyParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8b273-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADApplication [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b273-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b273-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzureRmADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b273-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b273-107">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b273-108">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b273-108">ApplicationDisplayNameParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8b273-109">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b273-109">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzureRmADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8b273-110">說明</span><span class="sxs-lookup"><span data-stu-id="8b273-110">DESCRIPTION</span></span>
<span data-ttu-id="8b273-111">列出現有的 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="8b273-111">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="8b273-112">應用程式查閱可以由 ObjectId、ApplicationId、IdentifierUri 或 DisplayName 來完成。</span><span class="sxs-lookup"><span data-stu-id="8b273-112">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="8b273-113">如果未提供任何參數，則它會提取租使用者下的所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="8b273-113">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="8b273-114">示例</span><span class="sxs-lookup"><span data-stu-id="8b273-114">EXAMPLES</span></span>

### <span data-ttu-id="8b273-115">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8b273-115">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Get-AzureRmADApplication
```

<span data-ttu-id="8b273-116">列出租使用者下的所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="8b273-116">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="8b273-117">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="8b273-117">--------------------------  Example 2  --------------------------</span></span>
```
PS E:\> Get-AzureRmADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="8b273-118">取得識別碼 uri 為 "" 的應用程式 http://mySecretApp1 。</span><span class="sxs-lookup"><span data-stu-id="8b273-118">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

## <span data-ttu-id="8b273-119">參數</span><span class="sxs-lookup"><span data-stu-id="8b273-119">PARAMETERS</span></span>

### <span data-ttu-id="8b273-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8b273-120">-ApplicationId</span></span>
<span data-ttu-id="8b273-121">要提取之應用程式的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="8b273-121">The application id of the application to fetch.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b273-122">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="8b273-122">-DisplayNameStartWith</span></span>
<span data-ttu-id="8b273-123">從顯示名稱開始提取所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="8b273-123">Fetch all applications starting with the display name.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b273-124">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="8b273-124">-IdentifierUri</span></span>
<span data-ttu-id="8b273-125">要提取之應用程式的唯一識別碼 Uri。</span><span class="sxs-lookup"><span data-stu-id="8b273-125">Unique identifier Uri of the application to fetch.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdentifierUriParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b273-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8b273-126">-ObjectId</span></span>
<span data-ttu-id="8b273-127">要提取之應用程式的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="8b273-127">The object id of the application to fetch.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b273-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b273-128">-DefaultProfile</span></span>
<span data-ttu-id="8b273-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8b273-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b273-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b273-130">CommonParameters</span></span>
<span data-ttu-id="8b273-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8b273-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b273-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8b273-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b273-133">輸入</span><span class="sxs-lookup"><span data-stu-id="8b273-133">INPUTS</span></span>

## <span data-ttu-id="8b273-134">輸出</span><span class="sxs-lookup"><span data-stu-id="8b273-134">OUTPUTS</span></span>

### <span data-ttu-id="8b273-135">[System.object]。清單 ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6 PSADApplication]</span><span class="sxs-lookup"><span data-stu-id="8b273-135">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication]</span></span>

## <span data-ttu-id="8b273-136">筆記</span><span class="sxs-lookup"><span data-stu-id="8b273-136">NOTES</span></span>

## <span data-ttu-id="8b273-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="8b273-137">RELATED LINKS</span></span>

[<span data-ttu-id="8b273-138">移除-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8b273-138">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="8b273-139">新-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8b273-139">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="8b273-140">AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8b273-140">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="8b273-141">移除-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="8b273-141">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="8b273-142">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="8b273-142">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="8b273-143">新-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="8b273-143">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)


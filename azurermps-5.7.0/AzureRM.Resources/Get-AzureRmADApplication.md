---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
ms.openlocfilehash: b44d3bbf7c594f5f9114488b536d28fd17fe56c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453083"
---
# <span data-ttu-id="ba8fc-101">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="ba8fc-101">Get-AzureRmADApplication</span></span>

## <span data-ttu-id="ba8fc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ba8fc-102">SYNOPSIS</span></span>
<span data-ttu-id="ba8fc-103">列出現有的 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="ba8fc-103">Lists existing azure active directory applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba8fc-104">句法</span><span class="sxs-lookup"><span data-stu-id="ba8fc-104">SYNTAX</span></span>

### <span data-ttu-id="ba8fc-105">EmptyParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ba8fc-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADApplication [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba8fc-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba8fc-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzureRmADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba8fc-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba8fc-107">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba8fc-108">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba8fc-108">ApplicationDisplayNameParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ba8fc-109">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba8fc-109">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzureRmADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba8fc-110">說明</span><span class="sxs-lookup"><span data-stu-id="ba8fc-110">DESCRIPTION</span></span>
<span data-ttu-id="ba8fc-111">列出現有的 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="ba8fc-111">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="ba8fc-112">應用程式查閱可以由 ObjectId、ApplicationId、IdentifierUri 或 DisplayName 來完成。</span><span class="sxs-lookup"><span data-stu-id="ba8fc-112">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="ba8fc-113">如果未提供任何參數，則它會提取租使用者下的所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="ba8fc-113">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="ba8fc-114">示例</span><span class="sxs-lookup"><span data-stu-id="ba8fc-114">EXAMPLES</span></span>

### <span data-ttu-id="ba8fc-115">範例1</span><span class="sxs-lookup"><span data-stu-id="ba8fc-115">Example 1</span></span>
```
PS E:\> Get-AzureRmADApplication
```

<span data-ttu-id="ba8fc-116">列出租使用者下的所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="ba8fc-116">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="ba8fc-117">範例2</span><span class="sxs-lookup"><span data-stu-id="ba8fc-117">Example 2</span></span>
```
PS E:\> Get-AzureRmADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="ba8fc-118">取得識別碼 uri 為 "" 的應用程式 http://mySecretApp1 。</span><span class="sxs-lookup"><span data-stu-id="ba8fc-118">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

## <span data-ttu-id="ba8fc-119">參數</span><span class="sxs-lookup"><span data-stu-id="ba8fc-119">PARAMETERS</span></span>

### <span data-ttu-id="ba8fc-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ba8fc-120">-ApplicationId</span></span>
<span data-ttu-id="ba8fc-121">要提取之應用程式的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="ba8fc-121">The application id of the application to fetch.</span></span>

```yaml
Type: Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba8fc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba8fc-122">-DefaultProfile</span></span>
<span data-ttu-id="ba8fc-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ba8fc-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba8fc-124">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="ba8fc-124">-DisplayNameStartWith</span></span>
<span data-ttu-id="ba8fc-125">從顯示名稱開始提取所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="ba8fc-125">Fetch all applications starting with the display name.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba8fc-126">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="ba8fc-126">-IdentifierUri</span></span>
<span data-ttu-id="ba8fc-127">要提取之應用程式的唯一識別碼 Uri。</span><span class="sxs-lookup"><span data-stu-id="ba8fc-127">Unique identifier Uri of the application to fetch.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdentifierUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba8fc-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ba8fc-128">-ObjectId</span></span>
<span data-ttu-id="ba8fc-129">要提取之應用程式的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="ba8fc-129">The object id of the application to fetch.</span></span>

```yaml
Type: Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba8fc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba8fc-130">CommonParameters</span></span>
<span data-ttu-id="ba8fc-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ba8fc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba8fc-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ba8fc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba8fc-133">輸入</span><span class="sxs-lookup"><span data-stu-id="ba8fc-133">INPUTS</span></span>

### <span data-ttu-id="ba8fc-134">所有</span><span class="sxs-lookup"><span data-stu-id="ba8fc-134">None</span></span>
<span data-ttu-id="ba8fc-135">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="ba8fc-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ba8fc-136">輸出</span><span class="sxs-lookup"><span data-stu-id="ba8fc-136">OUTPUTS</span></span>

### <span data-ttu-id="ba8fc-137">[System.object]。清單 ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6 PSADApplication]</span><span class="sxs-lookup"><span data-stu-id="ba8fc-137">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication]</span></span>

## <span data-ttu-id="ba8fc-138">筆記</span><span class="sxs-lookup"><span data-stu-id="ba8fc-138">NOTES</span></span>

## <span data-ttu-id="ba8fc-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba8fc-139">RELATED LINKS</span></span>

[<span data-ttu-id="ba8fc-140">移除-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ba8fc-140">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="ba8fc-141">新-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ba8fc-141">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="ba8fc-142">AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ba8fc-142">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="ba8fc-143">移除-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="ba8fc-143">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="ba8fc-144">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="ba8fc-144">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="ba8fc-145">新-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="ba8fc-145">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)


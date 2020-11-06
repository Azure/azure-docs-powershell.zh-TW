---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
ms.openlocfilehash: 34f4b85a299e714f524b1a4d33f2fb717483c377
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455615"
---
# <span data-ttu-id="e7d50-101">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e7d50-101">Get-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="e7d50-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e7d50-102">SYNOPSIS</span></span>
<span data-ttu-id="e7d50-103">篩選 active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="e7d50-103">Filters active directory service principals.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7d50-104">句法</span><span class="sxs-lookup"><span data-stu-id="e7d50-104">SYNTAX</span></span>

### <span data-ttu-id="e7d50-105">EmptyParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e7d50-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADServicePrincipal [-ServicePrincipalName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e7d50-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7d50-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -SearchString <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e7d50-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7d50-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7d50-108">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7d50-108">SPNParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e7d50-109">說明</span><span class="sxs-lookup"><span data-stu-id="e7d50-109">DESCRIPTION</span></span>
<span data-ttu-id="e7d50-110">篩選 active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="e7d50-110">Filters active directory service principals.</span></span>

## <span data-ttu-id="e7d50-111">示例</span><span class="sxs-lookup"><span data-stu-id="e7d50-111">EXAMPLES</span></span>

### <span data-ttu-id="e7d50-112">--------------------------使用 SPN--------------------------篩選服務主體</span><span class="sxs-lookup"><span data-stu-id="e7d50-112">--------------------------  Filters service principals using SPN  --------------------------</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal -SPN 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="e7d50-113">取得具有 36f81fc3-b00f-48cd-8218-3879f51ff39f SPN 的服務主體。</span><span class="sxs-lookup"><span data-stu-id="e7d50-113">Gets service principals with 36f81fc3-b00f-48cd-8218-3879f51ff39f SPN.</span></span>

### <span data-ttu-id="e7d50-114">--------------------------使用搜尋字串--------------------------篩選服務主體</span><span class="sxs-lookup"><span data-stu-id="e7d50-114">--------------------------  Filters service principals using Search String  --------------------------</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="e7d50-115">篩選所有顯示名稱以 "Web" 開頭的廣告服務主體。</span><span class="sxs-lookup"><span data-stu-id="e7d50-115">Filters all ad service principals that have display name starting with "Web".</span></span>

### <span data-ttu-id="e7d50-116">--------------------------清單廣告服務主體--------------------------</span><span class="sxs-lookup"><span data-stu-id="e7d50-116">--------------------------  List AD service principals  --------------------------</span></span>
```
PS C:\> Get-AzureRmADServicePrincipal
```

<span data-ttu-id="e7d50-117">取得所有廣告服務主體。</span><span class="sxs-lookup"><span data-stu-id="e7d50-117">Gets all AD service principals.</span></span>

## <span data-ttu-id="e7d50-118">參數</span><span class="sxs-lookup"><span data-stu-id="e7d50-118">PARAMETERS</span></span>

### <span data-ttu-id="e7d50-119">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e7d50-119">-ObjectId</span></span>
<span data-ttu-id="e7d50-120">服務主體的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="e7d50-120">Object id of the service principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7d50-121">-SearchString</span><span class="sxs-lookup"><span data-stu-id="e7d50-121">-SearchString</span></span>
<span data-ttu-id="e7d50-122">從這個值開始，提取所有顯示名稱的服務主體。</span><span class="sxs-lookup"><span data-stu-id="e7d50-122">Fetches all service principals that have the display name starting with this value.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7d50-123">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="e7d50-123">-ServicePrincipalName</span></span>
<span data-ttu-id="e7d50-124">服務的 SPN。</span><span class="sxs-lookup"><span data-stu-id="e7d50-124">SPN of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet
Aliases: SPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7d50-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7d50-125">-DefaultProfile</span></span>
<span data-ttu-id="e7d50-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e7d50-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7d50-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7d50-127">CommonParameters</span></span>
<span data-ttu-id="e7d50-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e7d50-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7d50-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e7d50-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7d50-130">輸入</span><span class="sxs-lookup"><span data-stu-id="e7d50-130">INPUTS</span></span>

## <span data-ttu-id="e7d50-131">輸出</span><span class="sxs-lookup"><span data-stu-id="e7d50-131">OUTPUTS</span></span>

### <span data-ttu-id="e7d50-132">[System.object]。清單 ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6 PSADServicePrincipal]</span><span class="sxs-lookup"><span data-stu-id="e7d50-132">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal]</span></span>

## <span data-ttu-id="e7d50-133">筆記</span><span class="sxs-lookup"><span data-stu-id="e7d50-133">NOTES</span></span>

## <span data-ttu-id="e7d50-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="e7d50-134">RELATED LINKS</span></span>

[<span data-ttu-id="e7d50-135">新-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e7d50-135">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="e7d50-136">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e7d50-136">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="e7d50-137">移除-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e7d50-137">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="e7d50-138">AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="e7d50-138">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="e7d50-139">AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e7d50-139">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)


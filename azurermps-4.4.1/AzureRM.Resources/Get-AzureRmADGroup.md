---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
ms.openlocfilehash: 1079486422da769863e86d3fc16d1c3ec65d6f5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448006"
---
# <span data-ttu-id="df051-101">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="df051-101">Get-AzureRmADGroup</span></span>

## <span data-ttu-id="df051-102">摘要</span><span class="sxs-lookup"><span data-stu-id="df051-102">SYNOPSIS</span></span>
<span data-ttu-id="df051-103">篩選 active directory 群組。</span><span class="sxs-lookup"><span data-stu-id="df051-103">Filters active directory groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df051-104">句法</span><span class="sxs-lookup"><span data-stu-id="df051-104">SYNTAX</span></span>

### <span data-ttu-id="df051-105">EmptyParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="df051-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df051-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="df051-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADGroup -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df051-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="df051-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df051-108">說明</span><span class="sxs-lookup"><span data-stu-id="df051-108">DESCRIPTION</span></span>
<span data-ttu-id="df051-109">篩選 active directory 群組。</span><span class="sxs-lookup"><span data-stu-id="df051-109">Filters active directory groups.</span></span>

## <span data-ttu-id="df051-110">示例</span><span class="sxs-lookup"><span data-stu-id="df051-110">EXAMPLES</span></span>

### <span data-ttu-id="df051-111">--------------------------使用物件識別碼篩選群組--------------------------</span><span class="sxs-lookup"><span data-stu-id="df051-111">--------------------------  Filters groups using object id  --------------------------</span></span>
```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="df051-112">取得含有85F89C90-780E-4AA6-9F4F-6F268D322EEE 識別碼的群組</span><span class="sxs-lookup"><span data-stu-id="df051-112">Gets group with 85F89C90-780E-4AA6-9F4F-6F268D322EEE id</span></span>

### <span data-ttu-id="df051-113">使用搜尋字串----------------------------------------------------篩選群組</span><span class="sxs-lookup"><span data-stu-id="df051-113">--------------------------  Filters groups using Search String  --------------------------</span></span>
```
PS C:\> Get-AzureRmADGroup -SearchString Joe
```

<span data-ttu-id="df051-114">篩選顯示名稱中含有 Joe 的所有廣告群組。</span><span class="sxs-lookup"><span data-stu-id="df051-114">Filters all ad groups that has Joe in the display name.</span></span>

### <span data-ttu-id="df051-115">--------------------------清單廣告群組--------------------------</span><span class="sxs-lookup"><span data-stu-id="df051-115">--------------------------  List AD groups  --------------------------</span></span>
```
PS C:\> Get-AzureRmADGroup
```

<span data-ttu-id="df051-116">取得所有廣告群組</span><span class="sxs-lookup"><span data-stu-id="df051-116">Gets all AD groups</span></span>

## <span data-ttu-id="df051-117">參數</span><span class="sxs-lookup"><span data-stu-id="df051-117">PARAMETERS</span></span>

### <span data-ttu-id="df051-118">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="df051-118">-ObjectId</span></span>
<span data-ttu-id="df051-119">群組的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="df051-119">Object id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="df051-120">-SearchString</span><span class="sxs-lookup"><span data-stu-id="df051-120">-SearchString</span></span>
<span data-ttu-id="df051-121">群組顯示名稱</span><span class="sxs-lookup"><span data-stu-id="df051-121">The group display name</span></span>

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

### <span data-ttu-id="df051-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df051-122">-DefaultProfile</span></span>
<span data-ttu-id="df051-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="df051-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df051-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df051-124">CommonParameters</span></span>
<span data-ttu-id="df051-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="df051-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df051-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="df051-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df051-127">輸入</span><span class="sxs-lookup"><span data-stu-id="df051-127">INPUTS</span></span>

## <span data-ttu-id="df051-128">輸出</span><span class="sxs-lookup"><span data-stu-id="df051-128">OUTPUTS</span></span>

### <span data-ttu-id="df051-129">[System.object]。清單 ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6 PSADGroup]</span><span class="sxs-lookup"><span data-stu-id="df051-129">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup]</span></span>

## <span data-ttu-id="df051-130">筆記</span><span class="sxs-lookup"><span data-stu-id="df051-130">NOTES</span></span>

## <span data-ttu-id="df051-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="df051-131">RELATED LINKS</span></span>

[<span data-ttu-id="df051-132">AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="df051-132">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="df051-133">AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="df051-133">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="df051-134">AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="df051-134">Get-AzureRmADGroupMember</span></span>](./Get-AzureRmADGroupMember.md)


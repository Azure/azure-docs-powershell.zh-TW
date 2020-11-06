---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7B8C8239-16A3-4C47-9D6F-DE31885532F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADServicePrincipal.md
ms.openlocfilehash: 853404bce6d45f2824c574b249c434ccebc281ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454112"
---
# <span data-ttu-id="30538-101">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="30538-101">Set-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="30538-102">摘要</span><span class="sxs-lookup"><span data-stu-id="30538-102">SYNOPSIS</span></span>
<span data-ttu-id="30538-103">更新現有的 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="30538-103">Updates an existing azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30538-104">句法</span><span class="sxs-lookup"><span data-stu-id="30538-104">SYNTAX</span></span>

### <span data-ttu-id="30538-105">SpObjectIdWithDisplayNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="30538-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Set-AzureRmADServicePrincipal -ObjectId <String> -DisplayName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30538-106">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="30538-106">SPNWithDisplayNameParameterSet</span></span>
```
Set-AzureRmADServicePrincipal -ServicePrincipalName <String> -DisplayName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30538-107">說明</span><span class="sxs-lookup"><span data-stu-id="30538-107">DESCRIPTION</span></span>
<span data-ttu-id="30538-108">更新現有的 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="30538-108">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="30538-109">若要更新與此服務主體相關聯的認證，請使用 New-AzureRmADSpCredential Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30538-109">To update the credentials associated with this service principal, please use New-AzureRmADSpCredential cmdlet.</span></span> <span data-ttu-id="30538-110">若要更新與基礎應用程式相關聯的屬性，請使用 Set-AzureRmADApplication Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30538-110">To update the properties associated with the underlying application, please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="30538-111">示例</span><span class="sxs-lookup"><span data-stu-id="30538-111">EXAMPLES</span></span>

### <span data-ttu-id="30538-112">範例1</span><span class="sxs-lookup"><span data-stu-id="30538-112">Example 1</span></span>
```
Set-AzureRmADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName "UpdatedNameForSp"
```

<span data-ttu-id="30538-113">使用指定的物件識別碼來更新服務主體的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="30538-113">Updates the display name for the service principal with specified object id.</span></span>

### <span data-ttu-id="30538-114">範例2</span><span class="sxs-lookup"><span data-stu-id="30538-114">Example 2</span></span>
```
Set-AzureRmADServicePrincipal -ServicePrincipalName "http://MyApp1" -DisplayName "UpdatedNameforSp"
```

<span data-ttu-id="30538-115">使用指定的服務主體名稱更新服務主體的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="30538-115">Updates the display name for the service principal with specified service principal name.</span></span>

## <span data-ttu-id="30538-116">參數</span><span class="sxs-lookup"><span data-stu-id="30538-116">PARAMETERS</span></span>

### <span data-ttu-id="30538-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30538-117">-DefaultProfile</span></span>
<span data-ttu-id="30538-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="30538-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30538-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="30538-119">-DisplayName</span></span>
<span data-ttu-id="30538-120">服務主體的新顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="30538-120">New display name for the service principal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30538-121">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="30538-121">-ObjectId</span></span>
<span data-ttu-id="30538-122">要更新的服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="30538-122">The object id of the service principal to update.</span></span>

```yaml
Type: String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30538-123">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="30538-123">-ServicePrincipalName</span></span>
<span data-ttu-id="30538-124">要更新的服務主體的 SPN。</span><span class="sxs-lookup"><span data-stu-id="30538-124">The SPN of service principal to update.</span></span>

```yaml
Type: String
Parameter Sets: SPNWithDisplayNameParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30538-125">-確認</span><span class="sxs-lookup"><span data-stu-id="30538-125">-Confirm</span></span>
<span data-ttu-id="30538-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="30538-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30538-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30538-127">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30538-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30538-128">CommonParameters</span></span>
<span data-ttu-id="30538-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="30538-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30538-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="30538-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30538-131">輸入</span><span class="sxs-lookup"><span data-stu-id="30538-131">INPUTS</span></span>

### <span data-ttu-id="30538-132">所有</span><span class="sxs-lookup"><span data-stu-id="30538-132">None</span></span>
<span data-ttu-id="30538-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="30538-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="30538-134">輸出</span><span class="sxs-lookup"><span data-stu-id="30538-134">OUTPUTS</span></span>

## <span data-ttu-id="30538-135">筆記</span><span class="sxs-lookup"><span data-stu-id="30538-135">NOTES</span></span>

## <span data-ttu-id="30538-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="30538-136">RELATED LINKS</span></span>

[<span data-ttu-id="30538-137">新-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="30538-137">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="30538-138">AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="30538-138">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="30538-139">移除-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="30538-139">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="30538-140">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="30538-140">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="30538-141">新-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="30538-141">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="30538-142">移除-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="30538-142">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)


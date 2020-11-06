---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7B8C8239-16A3-4C47-9D6F-DE31885532F4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADServicePrincipal.md
ms.openlocfilehash: 67af78e767b8da7764053e3652e25aef53f2877e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452352"
---
# <span data-ttu-id="845ad-101">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="845ad-101">Set-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="845ad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="845ad-102">SYNOPSIS</span></span>
<span data-ttu-id="845ad-103">更新現有的 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="845ad-103">Updates an existing azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="845ad-104">句法</span><span class="sxs-lookup"><span data-stu-id="845ad-104">SYNTAX</span></span>

### <span data-ttu-id="845ad-105">SpObjectIdWithDisplayNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="845ad-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Set-AzureRmADServicePrincipal -ObjectId <String> -DisplayName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="845ad-106">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="845ad-106">SPNWithDisplayNameParameterSet</span></span>
```
Set-AzureRmADServicePrincipal -ServicePrincipalName <String> -DisplayName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="845ad-107">說明</span><span class="sxs-lookup"><span data-stu-id="845ad-107">DESCRIPTION</span></span>
<span data-ttu-id="845ad-108">更新現有的 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="845ad-108">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="845ad-109">若要更新與此服務主體相關聯的認證，請使用 New-AzureRmADSpCredential Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="845ad-109">To update the credentials associated with this service principal, please use New-AzureRmADSpCredential cmdlet.</span></span> <span data-ttu-id="845ad-110">若要更新與基礎應用程式相關聯的屬性，請使用 Set-AzureRmADApplication Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="845ad-110">To update the properties associated with the underlying application, please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="845ad-111">示例</span><span class="sxs-lookup"><span data-stu-id="845ad-111">EXAMPLES</span></span>

### <span data-ttu-id="845ad-112">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="845ad-112">--------------------------  Example 1  --------------------------</span></span>
```
Set-AzureRmADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName "UpdatedNameForSp"
```

<span data-ttu-id="845ad-113">使用指定的物件識別碼來更新服務主體的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="845ad-113">Updates the display name for the service principal with specified object id.</span></span>

### <span data-ttu-id="845ad-114">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="845ad-114">--------------------------  Example 2  --------------------------</span></span>
```
Set-AzureRmADServicePrincipal -ServicePrincipalName "http://MyApp1" -DisplayName "UpdatedNameforSp"
```

<span data-ttu-id="845ad-115">使用指定的服務主體名稱更新服務主體的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="845ad-115">Updates the display name for the service principal with specified service principal name.</span></span>

## <span data-ttu-id="845ad-116">參數</span><span class="sxs-lookup"><span data-stu-id="845ad-116">PARAMETERS</span></span>

### <span data-ttu-id="845ad-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="845ad-117">-DisplayName</span></span>
<span data-ttu-id="845ad-118">服務主體的新顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="845ad-118">New display name for the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="845ad-119">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="845ad-119">-ObjectId</span></span>
<span data-ttu-id="845ad-120">要更新的服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="845ad-120">The object id of the service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="845ad-121">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="845ad-121">-ServicePrincipalName</span></span>
<span data-ttu-id="845ad-122">要更新的服務主體的 SPN。</span><span class="sxs-lookup"><span data-stu-id="845ad-122">The SPN of service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithDisplayNameParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="845ad-123">-確認</span><span class="sxs-lookup"><span data-stu-id="845ad-123">-Confirm</span></span>
<span data-ttu-id="845ad-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="845ad-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="845ad-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="845ad-125">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="845ad-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="845ad-126">-DefaultProfile</span></span>
<span data-ttu-id="845ad-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="845ad-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="845ad-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="845ad-128">CommonParameters</span></span>
<span data-ttu-id="845ad-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="845ad-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="845ad-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="845ad-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="845ad-131">輸入</span><span class="sxs-lookup"><span data-stu-id="845ad-131">INPUTS</span></span>

## <span data-ttu-id="845ad-132">輸出</span><span class="sxs-lookup"><span data-stu-id="845ad-132">OUTPUTS</span></span>

## <span data-ttu-id="845ad-133">筆記</span><span class="sxs-lookup"><span data-stu-id="845ad-133">NOTES</span></span>

## <span data-ttu-id="845ad-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="845ad-134">RELATED LINKS</span></span>

[<span data-ttu-id="845ad-135">新-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="845ad-135">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="845ad-136">AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="845ad-136">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="845ad-137">移除-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="845ad-137">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="845ad-138">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="845ad-138">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="845ad-139">新-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="845ad-139">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="845ad-140">移除-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="845ad-140">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)


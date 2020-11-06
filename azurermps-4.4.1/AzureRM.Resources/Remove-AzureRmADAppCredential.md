---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
ms.openlocfilehash: a5e99f045701a373e14990c25627696d40a04a37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452372"
---
# <span data-ttu-id="28b0e-101">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="28b0e-101">Remove-AzureRmADAppCredential</span></span>

## <span data-ttu-id="28b0e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="28b0e-102">SYNOPSIS</span></span>
<span data-ttu-id="28b0e-103">從應用程式移除認證。</span><span class="sxs-lookup"><span data-stu-id="28b0e-103">Removes a credential from an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28b0e-104">句法</span><span class="sxs-lookup"><span data-stu-id="28b0e-104">SYNTAX</span></span>

### <span data-ttu-id="28b0e-105">ApplicationObjectIdWithKeyIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="28b0e-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28b0e-106">ApplicationObjectIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="28b0e-106">ApplicationObjectIdWithAllParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <String> [-All] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28b0e-107">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28b0e-107">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28b0e-108">ApplicationIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="28b0e-108">ApplicationIdWithAllParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <String> [-All] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28b0e-109">說明</span><span class="sxs-lookup"><span data-stu-id="28b0e-109">DESCRIPTION</span></span>
<span data-ttu-id="28b0e-110">Remove-AzureRmADAppCredential Cmdlet 可以用來從應用程式中移除認證金鑰（如果遭到破壞或認證金鑰滾動更新到期的部分）。</span><span class="sxs-lookup"><span data-stu-id="28b0e-110">The Remove-AzureRmADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="28b0e-111">應用程式是透過提供物件識別碼或 AppId 來識別。</span><span class="sxs-lookup"><span data-stu-id="28b0e-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="28b0e-112">若要移除的認證是由其金鑰識別碼來識別，如果要移除個別認證或使用 [All] （全部）」開關來刪除與該應用程式相關聯的所有認證。</span><span class="sxs-lookup"><span data-stu-id="28b0e-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the application.</span></span>

## <span data-ttu-id="28b0e-113">示例</span><span class="sxs-lookup"><span data-stu-id="28b0e-113">EXAMPLES</span></span>

### <span data-ttu-id="28b0e-114">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="28b0e-114">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Remove-AzureRmADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="28b0e-115">這個命令會從應用程式中移除認證金鑰。</span><span class="sxs-lookup"><span data-stu-id="28b0e-115">This command removes a credential key from an application.</span></span>
<span data-ttu-id="28b0e-116">在這個範例中，將會從應用程式中移除 Id 為 "9044423a-60a3-45ac-9ab1-09534157ebb" 的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="28b0e-116">In this example, the key with Id "9044423a-60a3-45ac-9ab1-09534157ebb" will be removed from the application.</span></span>

### <span data-ttu-id="28b0e-117">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="28b0e-117">--------------------------  Example 2  --------------------------</span></span>
```
PS E:\> Remove-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -All
```

<span data-ttu-id="28b0e-118">這個命令會從應用程式中移除認證金鑰。</span><span class="sxs-lookup"><span data-stu-id="28b0e-118">This command removes a credential key from an application.</span></span>
<span data-ttu-id="28b0e-119">在這個範例中，所有認證將會從與 applicationId "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58" 相關聯的應用程式中移除。</span><span class="sxs-lookup"><span data-stu-id="28b0e-119">In this example, all credentials will be removed from the application associated with the applicationId "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".</span></span>

## <span data-ttu-id="28b0e-120">參數</span><span class="sxs-lookup"><span data-stu-id="28b0e-120">PARAMETERS</span></span>

### <span data-ttu-id="28b0e-121">-全部</span><span class="sxs-lookup"><span data-stu-id="28b0e-121">-All</span></span>
<span data-ttu-id="28b0e-122">[切換] 可移除與應用程式相關聯的所有認證。</span><span class="sxs-lookup"><span data-stu-id="28b0e-122">Switch to remove all the credentials associated with the application.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ApplicationObjectIdWithAllParameterSet, ApplicationIdWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b0e-123">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="28b0e-123">-ApplicationId</span></span>
<span data-ttu-id="28b0e-124">要從中移除認證的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="28b0e-124">The id of the application to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdWithKeyIdParameterSet, ApplicationIdWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b0e-125">-Force</span><span class="sxs-lookup"><span data-stu-id="28b0e-125">-Force</span></span>
<span data-ttu-id="28b0e-126">切換到 [刪除認證] 而不需確認。</span><span class="sxs-lookup"><span data-stu-id="28b0e-126">Switch to delete credential without a confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b0e-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="28b0e-127">-KeyId</span></span>
<span data-ttu-id="28b0e-128">指定要移除的認證金鑰。</span><span class="sxs-lookup"><span data-stu-id="28b0e-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="28b0e-129">應用程式的索引鍵識別碼可以使用 Get-AzureRmADAppCredential Cmdlet 取得。</span><span class="sxs-lookup"><span data-stu-id="28b0e-129">The key Ids for the application can be obtained using the Get-AzureRmADAppCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b0e-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="28b0e-130">-ObjectId</span></span>
<span data-ttu-id="28b0e-131">要從中移除認證之應用程式的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="28b0e-131">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationObjectIdWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b0e-132">-確認</span><span class="sxs-lookup"><span data-stu-id="28b0e-132">-Confirm</span></span>
<span data-ttu-id="28b0e-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="28b0e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28b0e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28b0e-134">-WhatIf</span></span>
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

### <span data-ttu-id="28b0e-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28b0e-135">-DefaultProfile</span></span>
<span data-ttu-id="28b0e-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="28b0e-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28b0e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28b0e-137">CommonParameters</span></span>
<span data-ttu-id="28b0e-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="28b0e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28b0e-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="28b0e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28b0e-140">輸入</span><span class="sxs-lookup"><span data-stu-id="28b0e-140">INPUTS</span></span>

## <span data-ttu-id="28b0e-141">輸出</span><span class="sxs-lookup"><span data-stu-id="28b0e-141">OUTPUTS</span></span>

## <span data-ttu-id="28b0e-142">筆記</span><span class="sxs-lookup"><span data-stu-id="28b0e-142">NOTES</span></span>

## <span data-ttu-id="28b0e-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="28b0e-143">RELATED LINKS</span></span>

[<span data-ttu-id="28b0e-144">AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="28b0e-144">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="28b0e-145">新-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="28b0e-145">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="28b0e-146">AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="28b0e-146">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

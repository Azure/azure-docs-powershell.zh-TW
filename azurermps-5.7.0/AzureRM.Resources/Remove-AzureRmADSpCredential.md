---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
ms.openlocfilehash: bfda87b4a0810dc440da63949d17f52cf611fa19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454136"
---
# <span data-ttu-id="c57e6-101">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="c57e6-101">Remove-AzureRmADSpCredential</span></span>

## <span data-ttu-id="c57e6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c57e6-102">SYNOPSIS</span></span>
<span data-ttu-id="c57e6-103">移除服務主體的認證。</span><span class="sxs-lookup"><span data-stu-id="c57e6-103">Removes a credential from a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c57e6-104">句法</span><span class="sxs-lookup"><span data-stu-id="c57e6-104">SYNTAX</span></span>

### <span data-ttu-id="c57e6-105">ObjectIdWithKeyIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c57e6-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADSpCredential -ObjectId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c57e6-106">ObjectIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="c57e6-106">ObjectIdWithAllParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ObjectId <String> [-All] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c57e6-107">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c57e6-107">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c57e6-108">SPNWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="c57e6-108">SPNWithAllParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> [-All] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c57e6-109">說明</span><span class="sxs-lookup"><span data-stu-id="c57e6-109">DESCRIPTION</span></span>
<span data-ttu-id="c57e6-110">Remove-AzureRmADSpCredential Cmdlet 可以用來移除服務主體（在安全性漏洞或認證金鑰滾動更新到期時）的認證金鑰。</span><span class="sxs-lookup"><span data-stu-id="c57e6-110">The Remove-AzureRmADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="c57e6-111">服務主體是透過提供物件識別碼或服務主體名稱 (SPN) 來加以識別。</span><span class="sxs-lookup"><span data-stu-id="c57e6-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>

<span data-ttu-id="c57e6-112">若要移除的認證是由其金鑰識別碼來識別，如果要移除個別認證或使用 [All] （全部）」開關來刪除與服務主體相關聯的所有認證。</span><span class="sxs-lookup"><span data-stu-id="c57e6-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="c57e6-113">示例</span><span class="sxs-lookup"><span data-stu-id="c57e6-113">EXAMPLES</span></span>

### <span data-ttu-id="c57e6-114">範例1</span><span class="sxs-lookup"><span data-stu-id="c57e6-114">Example 1</span></span>
```
PS E:\> Remove-AzureRmADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="c57e6-115">這個命令會從服務主體移除認證金鑰。</span><span class="sxs-lookup"><span data-stu-id="c57e6-115">This command removes a credential key from a service principal.</span></span>
<span data-ttu-id="c57e6-116">在這個範例中，將會從服務主體中移除 Id 為 "9044423a-60a3-45ac-9ab1-09534157ebb" 的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="c57e6-116">In this example, the key with Id "9044423a-60a3-45ac-9ab1-09534157ebb" will be removed from the service principal.</span></span>

### <span data-ttu-id="c57e6-117">範例2</span><span class="sxs-lookup"><span data-stu-id="c57e6-117">Example 2</span></span>
```
PS E:\> Remove-AzureRmADSpCredential -ServicePrincipalName http://test123 -All
```

<span data-ttu-id="c57e6-118">這個命令會從服務主體移除認證金鑰。</span><span class="sxs-lookup"><span data-stu-id="c57e6-118">This command removes a credential key from a service principal.</span></span>
<span data-ttu-id="c57e6-119">在這個範例中，所有認證將會從與服務主體名稱 "" 相關聯的服務主體中移除 http://test123 。</span><span class="sxs-lookup"><span data-stu-id="c57e6-119">In this example, all credentials will be removed from the service principal associated with the service principal name "http://test123".</span></span>

## <span data-ttu-id="c57e6-120">參數</span><span class="sxs-lookup"><span data-stu-id="c57e6-120">PARAMETERS</span></span>

### <span data-ttu-id="c57e6-121">-全部</span><span class="sxs-lookup"><span data-stu-id="c57e6-121">-All</span></span>
<span data-ttu-id="c57e6-122">[切換] 可移除與服務主體相關聯的所有認證。</span><span class="sxs-lookup"><span data-stu-id="c57e6-122">Switch to remove all the credentials associated with the service principal.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ObjectIdWithAllParameterSet, SPNWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c57e6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c57e6-123">-DefaultProfile</span></span>
<span data-ttu-id="c57e6-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c57e6-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c57e6-125">-Force</span><span class="sxs-lookup"><span data-stu-id="c57e6-125">-Force</span></span>
<span data-ttu-id="c57e6-126">切換到 [刪除認證] 而不需確認。</span><span class="sxs-lookup"><span data-stu-id="c57e6-126">Switch to delete credential without a confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c57e6-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="c57e6-127">-KeyId</span></span>
<span data-ttu-id="c57e6-128">指定要移除的認證金鑰。</span><span class="sxs-lookup"><span data-stu-id="c57e6-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="c57e6-129">服務主體的金鑰識別碼可以使用 Get-AzureRmADSpCredential Cmdlet 取得。</span><span class="sxs-lookup"><span data-stu-id="c57e6-129">The key Ids for a service principal can be obtained using the Get-AzureRmADSpCredential cmdlet.</span></span>

```yaml
Type: Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c57e6-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c57e6-130">-ObjectId</span></span>
<span data-ttu-id="c57e6-131">要從中移除認證的服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="c57e6-131">The object id of the service principal to remove the credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ObjectIdWithKeyIdParameterSet, ObjectIdWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c57e6-132">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="c57e6-132">-ServicePrincipalName</span></span>
<span data-ttu-id="c57e6-133">要從中移除認證的服務主體 (SPN) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="c57e6-133">The name (SPN) of the service principal to remove the credentials from.</span></span>

```yaml
Type: String
Parameter Sets: SPNWithKeyIdParameterSet, SPNWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c57e6-134">-確認</span><span class="sxs-lookup"><span data-stu-id="c57e6-134">-Confirm</span></span>
<span data-ttu-id="c57e6-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c57e6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c57e6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c57e6-136">-WhatIf</span></span>
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

### <span data-ttu-id="c57e6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c57e6-137">CommonParameters</span></span>
<span data-ttu-id="c57e6-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c57e6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c57e6-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c57e6-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c57e6-140">輸入</span><span class="sxs-lookup"><span data-stu-id="c57e6-140">INPUTS</span></span>

### <span data-ttu-id="c57e6-141">所有</span><span class="sxs-lookup"><span data-stu-id="c57e6-141">None</span></span>
<span data-ttu-id="c57e6-142">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="c57e6-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c57e6-143">輸出</span><span class="sxs-lookup"><span data-stu-id="c57e6-143">OUTPUTS</span></span>

## <span data-ttu-id="c57e6-144">筆記</span><span class="sxs-lookup"><span data-stu-id="c57e6-144">NOTES</span></span>

## <span data-ttu-id="c57e6-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="c57e6-145">RELATED LINKS</span></span>

[<span data-ttu-id="c57e6-146">AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="c57e6-146">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="c57e6-147">新-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="c57e6-147">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="c57e6-148">AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c57e6-148">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
ms.openlocfilehash: b71a25fa7e3e7c70b363b3462294e3c071a6ce86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906506"
---
# <span data-ttu-id="b3b81-101">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b3b81-101">Remove-AzADSpCredential</span></span>

## <span data-ttu-id="b3b81-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b3b81-102">SYNOPSIS</span></span>
<span data-ttu-id="b3b81-103">從服務主體移除認證。</span><span class="sxs-lookup"><span data-stu-id="b3b81-103">Removes a credential from a service principal.</span></span>

## <span data-ttu-id="b3b81-104">語法</span><span class="sxs-lookup"><span data-stu-id="b3b81-104">SYNTAX</span></span>

### <span data-ttu-id="b3b81-105">ObjectIdWithKeyIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b3b81-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADSpCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3b81-106">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3b81-106">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalName <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3b81-107">DisplayNameWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3b81-107">DisplayNameWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3b81-108">ServicePrincipalObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3b81-108">ServicePrincipalObjectParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3b81-109">描述</span><span class="sxs-lookup"><span data-stu-id="b3b81-109">DESCRIPTION</span></span>
<span data-ttu-id="b3b81-110">在Remove-AzADSpCredential或認證金鑰切換到期時，可以使用 Remove-AzADSpCredential Cmdlet 從服務主體移除認證金鑰。</span><span class="sxs-lookup"><span data-stu-id="b3b81-110">The Remove-AzADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="b3b81-111">服務主體是提供物件識別碼或服務主體名稱 (SPN) 。</span><span class="sxs-lookup"><span data-stu-id="b3b81-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>
<span data-ttu-id="b3b81-112">若要移除個別認證，或使用 'All' 切換來刪除與服務主體相關聯的所有認證，要移除的認證會以金鑰識別碼識別。</span><span class="sxs-lookup"><span data-stu-id="b3b81-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="b3b81-113">例子</span><span class="sxs-lookup"><span data-stu-id="b3b81-113">EXAMPLES</span></span>

### <span data-ttu-id="b3b81-114">範例 1：從服務主體移除特定認證</span><span class="sxs-lookup"><span data-stu-id="b3b81-114">Example 1: Remove a specific credential from a service principal</span></span>

```powershell
PS C:\> Remove-AzADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="b3b81-115">從服務主體移除具有金鑰識別碼 '9044423a-60a3-45ac-9ab1-09534157ebb'的認證，其物件識別碼為 '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'。</span><span class="sxs-lookup"><span data-stu-id="b3b81-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="b3b81-116">範例 2：從服務主體移除所有認證</span><span class="sxs-lookup"><span data-stu-id="b3b81-116">Example 2: Remove all credentials from a service principal</span></span>

```powershell
PS C:\> Remove-AzADSpCredential -ServicePrincipalName http://test123
```

<span data-ttu-id="b3b81-117">使用 SPN ""移除服務主體的所有 http://test123 認證。</span><span class="sxs-lookup"><span data-stu-id="b3b81-117">Removes all credentials from the service principal with the SPN "http://test123".</span></span>

### <span data-ttu-id="b3b81-118">範例 3：使用管道移除服務主體的所有認證</span><span class="sxs-lookup"><span data-stu-id="b3b81-118">Example 3: Remove all credentials from a service principal using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADSpCredential
```

<span data-ttu-id="b3b81-119">使用物件識別碼為 '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' 的服務主體，以及管道到 Remove-AzADSpCredential Cmdlet 以移除該服務主體的所有認證。</span><span class="sxs-lookup"><span data-stu-id="b3b81-119">Gets the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADSpCredential cmdlet to remove all credentials from that service principal.</span></span>

## <span data-ttu-id="b3b81-120">參數</span><span class="sxs-lookup"><span data-stu-id="b3b81-120">PARAMETERS</span></span>

### <span data-ttu-id="b3b81-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3b81-121">-DefaultProfile</span></span>
<span data-ttu-id="b3b81-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="b3b81-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3b81-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b3b81-123">-DisplayName</span></span>
<span data-ttu-id="b3b81-124">服務主體的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="b3b81-124">The display name of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b81-125">-強制</span><span class="sxs-lookup"><span data-stu-id="b3b81-125">-Force</span></span>
<span data-ttu-id="b3b81-126">切換以刪除認證而不進行確認。</span><span class="sxs-lookup"><span data-stu-id="b3b81-126">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="b3b81-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="b3b81-127">-KeyId</span></span>
<span data-ttu-id="b3b81-128">指定要移除的認證金鑰。</span><span class="sxs-lookup"><span data-stu-id="b3b81-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="b3b81-129">您可以使用 Cmdlet 取得服務主體Get-AzADSpCredential識別碼。</span><span class="sxs-lookup"><span data-stu-id="b3b81-129">The key Ids for a service principal can be obtained using the Get-AzADSpCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet, ServicePrincipalObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b81-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b3b81-130">-ObjectId</span></span>
<span data-ttu-id="b3b81-131">要從移除認證的服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="b3b81-131">The object id of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b81-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3b81-132">-PassThru</span></span>
<span data-ttu-id="b3b81-133">如果命令成功，指定此選項會返回 True。</span><span class="sxs-lookup"><span data-stu-id="b3b81-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="b3b81-134">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="b3b81-134">-ServicePrincipalName</span></span>
<span data-ttu-id="b3b81-135">SPN (SPN) 移除認證之服務主體的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3b81-135">The name (SPN) of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b81-136">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="b3b81-136">-ServicePrincipalObject</span></span>
<span data-ttu-id="b3b81-137">要從移除認證的服務主體物件。</span><span class="sxs-lookup"><span data-stu-id="b3b81-137">The service principal object to remove the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3b81-138">-確認</span><span class="sxs-lookup"><span data-stu-id="b3b81-138">-Confirm</span></span>
<span data-ttu-id="b3b81-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b3b81-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3b81-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3b81-140">-WhatIf</span></span>
<span data-ttu-id="b3b81-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b3b81-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3b81-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3b81-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3b81-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3b81-143">CommonParameters</span></span>
<span data-ttu-id="b3b81-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b3b81-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3b81-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3b81-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3b81-146">輸入</span><span class="sxs-lookup"><span data-stu-id="b3b81-146">INPUTS</span></span>

### <span data-ttu-id="b3b81-147">System.String</span><span class="sxs-lookup"><span data-stu-id="b3b81-147">System.String</span></span>

### <span data-ttu-id="b3b81-148">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b3b81-148">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="b3b81-149">System.Guid</span><span class="sxs-lookup"><span data-stu-id="b3b81-149">System.Guid</span></span>

## <span data-ttu-id="b3b81-150">輸出</span><span class="sxs-lookup"><span data-stu-id="b3b81-150">OUTPUTS</span></span>

### <span data-ttu-id="b3b81-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b3b81-151">System.Boolean</span></span>

## <span data-ttu-id="b3b81-152">筆記</span><span class="sxs-lookup"><span data-stu-id="b3b81-152">NOTES</span></span>

## <span data-ttu-id="b3b81-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3b81-153">RELATED LINKS</span></span>

[<span data-ttu-id="b3b81-154">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b3b81-154">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="b3b81-155">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b3b81-155">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="b3b81-156">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b3b81-156">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)


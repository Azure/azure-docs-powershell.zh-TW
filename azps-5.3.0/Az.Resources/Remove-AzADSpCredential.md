---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADSpCredential.md
ms.openlocfilehash: bcb33f87b85eb6ad5bce9ba812ebccb4d154e920
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435408"
---
# <span data-ttu-id="a12b9-101">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a12b9-101">Remove-AzADSpCredential</span></span>

## <span data-ttu-id="a12b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a12b9-102">SYNOPSIS</span></span>
<span data-ttu-id="a12b9-103">移除服務主體的認證。</span><span class="sxs-lookup"><span data-stu-id="a12b9-103">Removes a credential from a service principal.</span></span>

## <span data-ttu-id="a12b9-104">句法</span><span class="sxs-lookup"><span data-stu-id="a12b9-104">SYNTAX</span></span>

### <span data-ttu-id="a12b9-105">ObjectIdWithKeyIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a12b9-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzADSpCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a12b9-106">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a12b9-106">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalName <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a12b9-107">DisplayNameWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a12b9-107">DisplayNameWithKeyIdParameterSet</span></span>
```
Remove-AzADSpCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a12b9-108">ServicePrincipalObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a12b9-108">ServicePrincipalObjectParameterSet</span></span>
```
Remove-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a12b9-109">說明</span><span class="sxs-lookup"><span data-stu-id="a12b9-109">DESCRIPTION</span></span>
<span data-ttu-id="a12b9-110">Remove-AzADSpCredential Cmdlet 可以用來移除服務主體（在安全性漏洞或認證金鑰滾動更新到期時）的認證金鑰。</span><span class="sxs-lookup"><span data-stu-id="a12b9-110">The Remove-AzADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="a12b9-111">服務主體是透過提供物件識別碼或服務主體名稱 (SPN) 來加以識別。</span><span class="sxs-lookup"><span data-stu-id="a12b9-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>
<span data-ttu-id="a12b9-112">若要移除的認證是由其金鑰識別碼來識別，如果要移除個別認證或使用 [All] （全部）」開關來刪除與服務主體相關聯的所有認證。</span><span class="sxs-lookup"><span data-stu-id="a12b9-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="a12b9-113">示例</span><span class="sxs-lookup"><span data-stu-id="a12b9-113">EXAMPLES</span></span>

### <span data-ttu-id="a12b9-114">範例1：從服務主體移除特定認證</span><span class="sxs-lookup"><span data-stu-id="a12b9-114">Example 1: Remove a specific credential from a service principal</span></span>

```powershell
PS C:\> Remove-AzADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="a12b9-115">從具有物件 id "09534157ebb" 的服務主體中，移除具有金鑰識別碼 ' 9044423a-60a3-45ac-9ab1-7663d3fb-6f86-4352-9e6d-cf9d50d5ee82」的認證。</span><span class="sxs-lookup"><span data-stu-id="a12b9-115">Removes the credential with key id '9044423a-60a3-45ac-9ab1-09534157ebb' from the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82'.</span></span>

### <span data-ttu-id="a12b9-116">範例2：移除服務主體中的所有認證</span><span class="sxs-lookup"><span data-stu-id="a12b9-116">Example 2: Remove all credentials from a service principal</span></span>

```powershell
PS C:\> Remove-AzADSpCredential -ServicePrincipalName http://test123
```

<span data-ttu-id="a12b9-117">移除服務主體中具有 SPN "" 的所有認證 http://test123 。</span><span class="sxs-lookup"><span data-stu-id="a12b9-117">Removes all credentials from the service principal with the SPN "http://test123".</span></span>

### <span data-ttu-id="a12b9-118">範例3：使用管道移除服務主體中的所有認證</span><span class="sxs-lookup"><span data-stu-id="a12b9-118">Example 3: Remove all credentials from a service principal using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADSpCredential
```

<span data-ttu-id="a12b9-119">取得 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 Cmdlet 之物件識別碼 '」和 Remove-AzADSpCredential 管道的服務主體，以移除該服務主體的所有認證。</span><span class="sxs-lookup"><span data-stu-id="a12b9-119">Gets the service principal with object id '7663d3fb-6f86-4352-9e6d-cf9d50d5ee82' and pipes that to the Remove-AzADSpCredential cmdlet to remove all credentials from that service principal.</span></span>

## <span data-ttu-id="a12b9-120">參數</span><span class="sxs-lookup"><span data-stu-id="a12b9-120">PARAMETERS</span></span>

### <span data-ttu-id="a12b9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a12b9-121">-DefaultProfile</span></span>
<span data-ttu-id="a12b9-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a12b9-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a12b9-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a12b9-123">-DisplayName</span></span>
<span data-ttu-id="a12b9-124">服務主體的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a12b9-124">The display name of the service principal.</span></span>

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

### <span data-ttu-id="a12b9-125">-Force</span><span class="sxs-lookup"><span data-stu-id="a12b9-125">-Force</span></span>
<span data-ttu-id="a12b9-126">切換到 [刪除認證] 而不需確認。</span><span class="sxs-lookup"><span data-stu-id="a12b9-126">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="a12b9-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="a12b9-127">-KeyId</span></span>
<span data-ttu-id="a12b9-128">指定要移除的認證金鑰。</span><span class="sxs-lookup"><span data-stu-id="a12b9-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="a12b9-129">服務主體的金鑰識別碼可以使用 Get-AzADSpCredential Cmdlet 取得。</span><span class="sxs-lookup"><span data-stu-id="a12b9-129">The key Ids for a service principal can be obtained using the Get-AzADSpCredential cmdlet.</span></span>

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

### <span data-ttu-id="a12b9-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a12b9-130">-ObjectId</span></span>
<span data-ttu-id="a12b9-131">要從中移除認證的服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="a12b9-131">The object id of the service principal to remove the credentials from.</span></span>

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

### <span data-ttu-id="a12b9-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a12b9-132">-PassThru</span></span>
<span data-ttu-id="a12b9-133">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="a12b9-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="a12b9-134">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="a12b9-134">-ServicePrincipalName</span></span>
<span data-ttu-id="a12b9-135">要從中移除認證的服務主體 (SPN) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="a12b9-135">The name (SPN) of the service principal to remove the credentials from.</span></span>

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

### <span data-ttu-id="a12b9-136">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="a12b9-136">-ServicePrincipalObject</span></span>
<span data-ttu-id="a12b9-137">要從中移除認證的服務主體物件。</span><span class="sxs-lookup"><span data-stu-id="a12b9-137">The service principal object to remove the credentials from.</span></span>

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

### <span data-ttu-id="a12b9-138">-確認</span><span class="sxs-lookup"><span data-stu-id="a12b9-138">-Confirm</span></span>
<span data-ttu-id="a12b9-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a12b9-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a12b9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a12b9-140">-WhatIf</span></span>
<span data-ttu-id="a12b9-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a12b9-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a12b9-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a12b9-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a12b9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a12b9-143">CommonParameters</span></span>
<span data-ttu-id="a12b9-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a12b9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a12b9-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a12b9-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a12b9-146">輸入</span><span class="sxs-lookup"><span data-stu-id="a12b9-146">INPUTS</span></span>

### <span data-ttu-id="a12b9-147">System.object</span><span class="sxs-lookup"><span data-stu-id="a12b9-147">System.String</span></span>

### <span data-ttu-id="a12b9-148">PSADServicePrincipal （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="a12b9-148">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="a12b9-149">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="a12b9-149">System.Guid</span></span>

## <span data-ttu-id="a12b9-150">輸出</span><span class="sxs-lookup"><span data-stu-id="a12b9-150">OUTPUTS</span></span>

### <span data-ttu-id="a12b9-151">System.object</span><span class="sxs-lookup"><span data-stu-id="a12b9-151">System.Boolean</span></span>

## <span data-ttu-id="a12b9-152">筆記</span><span class="sxs-lookup"><span data-stu-id="a12b9-152">NOTES</span></span>

## <span data-ttu-id="a12b9-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="a12b9-153">RELATED LINKS</span></span>

[<span data-ttu-id="a12b9-154">AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a12b9-154">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="a12b9-155">新-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="a12b9-155">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="a12b9-156">AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="a12b9-156">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)


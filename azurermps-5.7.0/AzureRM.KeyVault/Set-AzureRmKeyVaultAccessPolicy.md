---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurermkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: 20a36e35c509ecca889d4059bd7e74ccafa22dc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447777"
---
# <span data-ttu-id="f446e-101">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f446e-101">Set-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="f446e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f446e-102">SYNOPSIS</span></span>
<span data-ttu-id="f446e-103">授與修改使用者、應用程式或安全性群組的現有許可權，以使用金鑰保存庫執行作業。</span><span class="sxs-lookup"><span data-stu-id="f446e-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f446e-104">句法</span><span class="sxs-lookup"><span data-stu-id="f446e-104">SYNTAX</span></span>

### <span data-ttu-id="f446e-105">ByUserPrincipalName (預設) </span><span class="sxs-lookup"><span data-stu-id="f446e-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f446e-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="f446e-106">ByObjectId</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f446e-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f446e-107">ByServicePrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f446e-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="f446e-108">ByEmailAddress</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f446e-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="f446e-109">ForVault</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f446e-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="f446e-110">InputObjectByObjectId</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f446e-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f446e-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f446e-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="f446e-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f446e-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="f446e-113">InputObjectByEmailAddress</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f446e-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="f446e-114">InputObjectForVault</span></span>
```
Set-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f446e-115">說明</span><span class="sxs-lookup"><span data-stu-id="f446e-115">DESCRIPTION</span></span>
<span data-ttu-id="f446e-116">**AzureRmKeyVaultAccessPolicy** Cmdlet 會授權或修改使用者、應用程式或安全性群組的現有許可權，以使用金鑰保存庫執行指定的作業。</span><span class="sxs-lookup"><span data-stu-id="f446e-116">The **Set-AzureRmKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="f446e-117">它不會修改其他使用者、應用程式或安全性群組在主要電子倉庫上所擁有的許可權。</span><span class="sxs-lookup"><span data-stu-id="f446e-117">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>

<span data-ttu-id="f446e-118">如果您要設定安全性群組的許可權，此操作只會影響該安全性群組中的使用者。</span><span class="sxs-lookup"><span data-stu-id="f446e-118">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>

<span data-ttu-id="f446e-119">下列目錄必須都是相同的 Azure 目錄：</span><span class="sxs-lookup"><span data-stu-id="f446e-119">The following directories must all be the same Azure directory:</span></span> 
- <span data-ttu-id="f446e-120">存放主要電子倉庫之 Azure 訂閱的預設目錄。</span><span class="sxs-lookup"><span data-stu-id="f446e-120">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="f446e-121">包含您要授予其許可權之使用者或應用程式群組的 Azure 目錄。</span><span class="sxs-lookup"><span data-stu-id="f446e-121">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>

<span data-ttu-id="f446e-122">不符合這些條件的案例範例，且這個 Cmdlet 將無法運作：</span><span class="sxs-lookup"><span data-stu-id="f446e-122">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span> 

- <span data-ttu-id="f446e-123">授權其他組織的使用者管理您的主要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="f446e-123">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="f446e-124">每個組織都有自己的目錄。</span><span class="sxs-lookup"><span data-stu-id="f446e-124">Each organization has its own directory.</span></span> 
- <span data-ttu-id="f446e-125">您的 Azure 帳戶有多個目錄。</span><span class="sxs-lookup"><span data-stu-id="f446e-125">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="f446e-126">如果您在預設目錄以外的目錄中登錄應用程式，您就無法授權該應用程式使用您的金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="f446e-126">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="f446e-127">應用程式必須位於預設目錄中。</span><span class="sxs-lookup"><span data-stu-id="f446e-127">The application must be in the default directory.</span></span>

<span data-ttu-id="f446e-128">請注意，雖然為這個 Cmdlet 指定 [資源群組] 是選擇性的，但您應該這麼做，以取得較佳的效能。</span><span class="sxs-lookup"><span data-stu-id="f446e-128">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="f446e-129">示例</span><span class="sxs-lookup"><span data-stu-id="f446e-129">EXAMPLES</span></span>

### <span data-ttu-id="f446e-130">範例1：針對金鑰電子倉庫的使用者授與許可權，並修改許可權</span><span class="sxs-lookup"><span data-stu-id="f446e-130">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets set,delete
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru
```

<span data-ttu-id="f446e-131">第一個命令會在您的 Azure Active Directory 中為使用者授予許可權， PattiFuller@contoso.com 以在名為 Contoso03Vault 的金鑰保存庫中執行金鑰和密碼的操作。</span><span class="sxs-lookup"><span data-stu-id="f446e-131">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span>

<span data-ttu-id="f446e-132">第二個命令會修改 PattiFuller@contoso.com 在第一個命令中所授的許可權，現在允許取得機密，除了設定及刪除密碼以外。</span><span class="sxs-lookup"><span data-stu-id="f446e-132">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="f446e-133">此命令之後，對主要作業的許可權會保持不變。</span><span class="sxs-lookup"><span data-stu-id="f446e-133">The permissions to key operations remain unchanged after this command.</span></span> <span data-ttu-id="f446e-134">*PassThru* 參數會產生 Cmdlet 傳回的更新物件。</span><span class="sxs-lookup"><span data-stu-id="f446e-134">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

<span data-ttu-id="f446e-135">最後一個命令會進一步修改現有的許可權，以 PattiFuller@contoso.com 移除擁有權限的主要操作。</span><span class="sxs-lookup"><span data-stu-id="f446e-135">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="f446e-136">此命令之後，機密作業的許可權會保持不變。</span><span class="sxs-lookup"><span data-stu-id="f446e-136">The permissions to secret operations remain unchanged after this command.</span></span> <span data-ttu-id="f446e-137">*PassThru* 參數會產生 Cmdlet 傳回的更新物件。</span><span class="sxs-lookup"><span data-stu-id="f446e-137">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

### <span data-ttu-id="f446e-138">範例2：將應用程式服務主體的許可權授予讀取及撰寫機密的許可權</span><span class="sxs-lookup"><span data-stu-id="f446e-138">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="f446e-139">這個命令會為應用程式授予一個名為 Contoso03Vault 的金鑰保存庫的許可權。</span><span class="sxs-lookup"><span data-stu-id="f446e-139">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span> 

<span data-ttu-id="f446e-140">*ServicePrincipalName* 參數會指定應用程式。</span><span class="sxs-lookup"><span data-stu-id="f446e-140">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="f446e-141">應用程式必須在您的 Azure Active Directory 中註冊。</span><span class="sxs-lookup"><span data-stu-id="f446e-141">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="f446e-142">*ServicePrincipalName* 參數的值必須是應用程式的服務主體名稱或應用程式識別碼 GUID。</span><span class="sxs-lookup"><span data-stu-id="f446e-142">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>

<span data-ttu-id="f446e-143">這個範例會指定服務主體名稱 http://payroll.contoso.com ，且命令會授與寫入密碼的應用程式許可權。</span><span class="sxs-lookup"><span data-stu-id="f446e-143">This example specifies the service principal name http://payroll.contoso.com, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="f446e-144">範例3：使用物件識別碼為應用程式授與許可權</span><span class="sxs-lookup"><span data-stu-id="f446e-144">Example 3: Grant permissions for an application using its object ID</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="f446e-145">這個命令會授與寫入密碼的應用程式許可權。</span><span class="sxs-lookup"><span data-stu-id="f446e-145">This command grants the application permissions to read and write secrets.</span></span>

<span data-ttu-id="f446e-146">這個範例會使用應用程式服務主體的物件識別碼來指定應用程式。</span><span class="sxs-lookup"><span data-stu-id="f446e-146">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="f446e-147">範例4：為使用者主要名稱授與許可權</span><span class="sxs-lookup"><span data-stu-id="f446e-147">Example 4: Grant permissions for a user principal name</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="f446e-148">這個命令會針對針對密碼存取權的指定使用者主要名稱，授與 [取得]、[清單] 和 [設定] 許可權。</span><span class="sxs-lookup"><span data-stu-id="f446e-148">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="f446e-149">範例5：讓 Microsoft 能從金鑰保存庫取得機密。計算資源提供者</span><span class="sxs-lookup"><span data-stu-id="f446e-149">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="f446e-150">這個命令會授與 Microsoft. 計算資源提供者在 Contoso03Vault 金鑰保存庫中檢索的密碼許可權。</span><span class="sxs-lookup"><span data-stu-id="f446e-150">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="f446e-151">範例6：授與安全性群組的許可權</span><span class="sxs-lookup"><span data-stu-id="f446e-151">Example 6: Grant permissions to a security group</span></span>
```
PS C:\>Get-AzureRmADGroup
PS C:\> Set-AzureRmKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzureRmADGroup -SearchString 'group2')[0].Id -PermissionsToKeys All -PermissionsToSecrets All
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
group1                                                        96a0daa6-9841-4a9c-bdeb-e7062276c688
group2                                                        b8a401eb-63ad-4a30-b0e1-a7461969fe54
group3                                                        da07a6be-2c1e-4e42-934d-ceb57cf652b4
```

<span data-ttu-id="f446e-152">第一個命令使用 Get-AzureRmADGroup Cmdlet 來取得所有 Active Directory 群組。</span><span class="sxs-lookup"><span data-stu-id="f446e-152">The first command uses the Get-AzureRmADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="f446e-153">從輸出中，您會看到3個群組傳回、命名為 [ **group1** ]、[ **group2** ] 和 [ **group3** ]。</span><span class="sxs-lookup"><span data-stu-id="f446e-153">From the output, you see 3 groups returned, named **group1** , **group2** , and **group3**.</span></span> <span data-ttu-id="f446e-154">多個群組可以有相同的名稱，但永遠都是唯一的 ObjectId。</span><span class="sxs-lookup"><span data-stu-id="f446e-154">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="f446e-155">如果傳回多個同名的群組，請使用輸出中的 ObjectId 來識別您想要使用的群組。</span><span class="sxs-lookup"><span data-stu-id="f446e-155">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>

<span data-ttu-id="f446e-156">接著，您可以使用此命令的輸出，將 group2 的許可權授 Set-AzureRmKeyVaultAccessPolicy 與您的主要保存庫（名為 **myownvault** ）。</span><span class="sxs-lookup"><span data-stu-id="f446e-156">You then use the output of this command with Set-AzureRmKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="f446e-157">這個範例列舉了相同命令列中以「group2」為內聯的群組。</span><span class="sxs-lookup"><span data-stu-id="f446e-157">This example enumerates the groups named 'group2' inline in the same command line.</span></span>

<span data-ttu-id="f446e-158">傳回的清單中可能有多個名為「group2」的群組。</span><span class="sxs-lookup"><span data-stu-id="f446e-158">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="f446e-159">這個範例會選取第一個專案，並在 \[ \] 傳回的清單中以 index 0 所示。</span><span class="sxs-lookup"><span data-stu-id="f446e-159">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="f446e-160">範例7：授與客戶管理的租使用者金鑰 (BYOK) 的 Azure 資訊保護存取權</span><span class="sxs-lookup"><span data-stu-id="f446e-160">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="f446e-161">這個命令授權 Azure 資訊保護使用客戶管理的金鑰 (將您自己的金鑰或 "BYOK" 案例) 為 Azure 資訊保護租使用者金鑰。</span><span class="sxs-lookup"><span data-stu-id="f446e-161">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>

<span data-ttu-id="f446e-162">當您執行此命令時，請指定您自己的金鑰保存庫名稱，但您必須指定具有 GUID **00000012-0000-0000-c000-000000000000** 的 *ServicePrincipalName* 參數，並指定範例中的許可權。</span><span class="sxs-lookup"><span data-stu-id="f446e-162">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="f446e-163">參數</span><span class="sxs-lookup"><span data-stu-id="f446e-163">PARAMETERS</span></span>

### <span data-ttu-id="f446e-164">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f446e-164">-ApplicationId</span></span>
<span data-ttu-id="f446e-165">以供日後使用。</span><span class="sxs-lookup"><span data-stu-id="f446e-165">For future use.</span></span>

```yaml
Type: Guid
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f446e-166">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="f446e-166">-BypassObjectIdValidation</span></span>
<span data-ttu-id="f446e-167">可讓您指定物件識別碼，而不驗證該物件存在於 Azure Active Directory 中。</span><span class="sxs-lookup"><span data-stu-id="f446e-167">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>

<span data-ttu-id="f446e-168">如果您想要將您的金鑰保存庫存取權授予參照來自其他 Azure 租使用者的委派安全性群組的物件識別碼，請使用此參數。</span><span class="sxs-lookup"><span data-stu-id="f446e-168">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f446e-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f446e-169">-DefaultProfile</span></span>
<span data-ttu-id="f446e-170">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f446e-170">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f446e-171">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="f446e-171">-EmailAddress</span></span>
<span data-ttu-id="f446e-172">指定要授與許可權的使用者的使用者電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="f446e-172">Specifies the user email address of the user to whom to grant permissions.</span></span>

<span data-ttu-id="f446e-173">此電子郵件地址必須存在於與目前訂閱相關聯的目錄中，且必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="f446e-173">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

```yaml
Type: String
Parameter Sets: ByEmailAddress, InputObjectByEmailAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f446e-174">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="f446e-174">-EnabledForDeployment</span></span>
<span data-ttu-id="f446e-175">當在資源建立期間參照此金鑰保存庫時，可使用 Microsoft. 計算資源提供者來從此金鑰保存庫中取得機密資訊，例如建立虛擬機器時。</span><span class="sxs-lookup"><span data-stu-id="f446e-175">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f446e-176">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="f446e-176">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="f446e-177">讓 Azure 磁片加密服務從此金鑰保存庫取得機密和解除解包金鑰。</span><span class="sxs-lookup"><span data-stu-id="f446e-177">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f446e-178">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="f446e-178">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="f446e-179">在範本部署中參照此金鑰保存庫時，允許 Azure 資源管理員從該金鑰保存庫取得機密。</span><span class="sxs-lookup"><span data-stu-id="f446e-179">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f446e-180">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f446e-180">-InputObject</span></span>
<span data-ttu-id="f446e-181">金鑰保存庫物件</span><span class="sxs-lookup"><span data-stu-id="f446e-181">Key Vault Object</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f446e-182">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f446e-182">-ObjectId</span></span>
<span data-ttu-id="f446e-183">指定 Azure Active Directory 中要授與許可權的使用者或服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="f446e-183">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f446e-184">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f446e-184">-PassThru</span></span>
<span data-ttu-id="f446e-185">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="f446e-185">Returns an object representing the item with which you are working.</span></span>

<span data-ttu-id="f446e-186">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="f446e-186">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f446e-187">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="f446e-187">-PermissionsToCertificates</span></span>
<span data-ttu-id="f446e-188">指定要授與使用者或服務主體的憑證許可權陣列。</span><span class="sxs-lookup"><span data-stu-id="f446e-188">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="f446e-189">此參數可接受的值：</span><span class="sxs-lookup"><span data-stu-id="f446e-189">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="f446e-190">獲取</span><span class="sxs-lookup"><span data-stu-id="f446e-190">Get</span></span>
- <span data-ttu-id="f446e-191">清單</span><span class="sxs-lookup"><span data-stu-id="f446e-191">List</span></span>
- <span data-ttu-id="f446e-192">Delete</span><span class="sxs-lookup"><span data-stu-id="f446e-192">Delete</span></span>
- <span data-ttu-id="f446e-193">建立</span><span class="sxs-lookup"><span data-stu-id="f446e-193">Create</span></span>
- <span data-ttu-id="f446e-194">Import</span><span class="sxs-lookup"><span data-stu-id="f446e-194">Import</span></span>
- <span data-ttu-id="f446e-195">時更新</span><span class="sxs-lookup"><span data-stu-id="f446e-195">Update</span></span>
- <span data-ttu-id="f446e-196">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="f446e-196">Managecontacts</span></span>
- <span data-ttu-id="f446e-197">Getissuers</span><span class="sxs-lookup"><span data-stu-id="f446e-197">Getissuers</span></span>
- <span data-ttu-id="f446e-198">Listissuers</span><span class="sxs-lookup"><span data-stu-id="f446e-198">Listissuers</span></span>
- <span data-ttu-id="f446e-199">Setissuers</span><span class="sxs-lookup"><span data-stu-id="f446e-199">Setissuers</span></span>
- <span data-ttu-id="f446e-200">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="f446e-200">Deleteissuers</span></span>
- <span data-ttu-id="f446e-201">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="f446e-201">Manageissuers</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f446e-202">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="f446e-202">-PermissionsToKeys</span></span>
<span data-ttu-id="f446e-203">指定要授與使用者或服務主體的主要操作許可權陣列。</span><span class="sxs-lookup"><span data-stu-id="f446e-203">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="f446e-204">此參數可接受的值：</span><span class="sxs-lookup"><span data-stu-id="f446e-204">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="f446e-205">對</span><span class="sxs-lookup"><span data-stu-id="f446e-205">Decrypt</span></span>
- <span data-ttu-id="f446e-206">進行</span><span class="sxs-lookup"><span data-stu-id="f446e-206">Encrypt</span></span>
- <span data-ttu-id="f446e-207">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="f446e-207">UnwrapKey</span></span>
- <span data-ttu-id="f446e-208">WrapKey</span><span class="sxs-lookup"><span data-stu-id="f446e-208">WrapKey</span></span>
- <span data-ttu-id="f446e-209">是否</span><span class="sxs-lookup"><span data-stu-id="f446e-209">Verify</span></span>
- <span data-ttu-id="f446e-210">母音</span><span class="sxs-lookup"><span data-stu-id="f446e-210">Sign</span></span>
- <span data-ttu-id="f446e-211">獲取</span><span class="sxs-lookup"><span data-stu-id="f446e-211">Get</span></span>
- <span data-ttu-id="f446e-212">清單</span><span class="sxs-lookup"><span data-stu-id="f446e-212">List</span></span>
- <span data-ttu-id="f446e-213">時更新</span><span class="sxs-lookup"><span data-stu-id="f446e-213">Update</span></span>
- <span data-ttu-id="f446e-214">建立</span><span class="sxs-lookup"><span data-stu-id="f446e-214">Create</span></span>
- <span data-ttu-id="f446e-215">Import</span><span class="sxs-lookup"><span data-stu-id="f446e-215">Import</span></span>
- <span data-ttu-id="f446e-216">Delete</span><span class="sxs-lookup"><span data-stu-id="f446e-216">Delete</span></span>
- <span data-ttu-id="f446e-217">備份</span><span class="sxs-lookup"><span data-stu-id="f446e-217">Backup</span></span>
- <span data-ttu-id="f446e-218">還原</span><span class="sxs-lookup"><span data-stu-id="f446e-218">Restore</span></span>
- <span data-ttu-id="f446e-219">找回</span><span class="sxs-lookup"><span data-stu-id="f446e-219">Recover</span></span>
- <span data-ttu-id="f446e-220">立即</span><span class="sxs-lookup"><span data-stu-id="f446e-220">Purge</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f446e-221">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="f446e-221">-PermissionsToSecrets</span></span>
<span data-ttu-id="f446e-222">指定要授與使用者或服務主體的機密操作許可權陣列。</span><span class="sxs-lookup"><span data-stu-id="f446e-222">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="f446e-223">此參數可接受的值：</span><span class="sxs-lookup"><span data-stu-id="f446e-223">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="f446e-224">獲取</span><span class="sxs-lookup"><span data-stu-id="f446e-224">Get</span></span>
- <span data-ttu-id="f446e-225">清單</span><span class="sxs-lookup"><span data-stu-id="f446e-225">List</span></span>
- <span data-ttu-id="f446e-226">設定</span><span class="sxs-lookup"><span data-stu-id="f446e-226">Set</span></span>
- <span data-ttu-id="f446e-227">Delete</span><span class="sxs-lookup"><span data-stu-id="f446e-227">Delete</span></span>
- <span data-ttu-id="f446e-228">備份</span><span class="sxs-lookup"><span data-stu-id="f446e-228">Backup</span></span>
- <span data-ttu-id="f446e-229">還原</span><span class="sxs-lookup"><span data-stu-id="f446e-229">Restore</span></span>
- <span data-ttu-id="f446e-230">找回</span><span class="sxs-lookup"><span data-stu-id="f446e-230">Recover</span></span>
- <span data-ttu-id="f446e-231">立即</span><span class="sxs-lookup"><span data-stu-id="f446e-231">Purge</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: get, list, set, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f446e-232">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="f446e-232">-PermissionsToStorage</span></span>
<span data-ttu-id="f446e-233">指定受管理的儲存帳戶和 SaS 定義操作許可權，以授與使用者或服務主體。</span><span class="sxs-lookup"><span data-stu-id="f446e-233">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

```yaml
Type: String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress
Aliases:
Accepted values: get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f446e-234">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f446e-234">-ResourceGroupName</span></span>
<span data-ttu-id="f446e-235">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f446e-235">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f446e-236">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f446e-236">-ServicePrincipalName</span></span>
<span data-ttu-id="f446e-237">指定要授與許可權之應用程式的服務主體名稱。</span><span class="sxs-lookup"><span data-stu-id="f446e-237">Specifies the service principal name of the application to which to grant permissions.</span></span>

<span data-ttu-id="f446e-238">指定在 AzureActive 目錄中為應用程式註冊的應用程式識別碼（也稱為「用戶端識別碼」）。</span><span class="sxs-lookup"><span data-stu-id="f446e-238">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="f446e-239">具有此參數指定之服務主體名稱的應用程式，必須在包含您目前訂閱的 Azure 目錄中註冊。</span><span class="sxs-lookup"><span data-stu-id="f446e-239">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByServicePrincipalName, InputObjectByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f446e-240">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="f446e-240">-UserPrincipalName</span></span>
<span data-ttu-id="f446e-241">指定要授與許可權的使用者的使用者主要名稱。</span><span class="sxs-lookup"><span data-stu-id="f446e-241">Specifies the user principal name of the user to whom to grant permissions.</span></span>

<span data-ttu-id="f446e-242">此使用者主要名稱必須存在於與目前訂閱相關聯的目錄中。</span><span class="sxs-lookup"><span data-stu-id="f446e-242">This user principal name must exist in the directory associated with the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, InputObjectByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f446e-243">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f446e-243">-VaultName</span></span>
<span data-ttu-id="f446e-244">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="f446e-244">Specifies the name of a key vault.</span></span>

<span data-ttu-id="f446e-245">這個 Cmdlet 會修改此參數指定之金鑰保存庫的存取原則。</span><span class="sxs-lookup"><span data-stu-id="f446e-245">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f446e-246">-確認</span><span class="sxs-lookup"><span data-stu-id="f446e-246">-Confirm</span></span>
<span data-ttu-id="f446e-247">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f446e-247">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f446e-248">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f446e-248">-WhatIf</span></span>
<span data-ttu-id="f446e-249">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f446e-249">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f446e-250">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f446e-250">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f446e-251">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f446e-251">CommonParameters</span></span>
<span data-ttu-id="f446e-252">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f446e-252">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f446e-253">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f446e-253">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f446e-254">輸入</span><span class="sxs-lookup"><span data-stu-id="f446e-254">INPUTS</span></span>

### <span data-ttu-id="f446e-255">字串、Guid、String []、Switch</span><span class="sxs-lookup"><span data-stu-id="f446e-255">String, Guid, String[], Switch</span></span>

## <span data-ttu-id="f446e-256">輸出</span><span class="sxs-lookup"><span data-stu-id="f446e-256">OUTPUTS</span></span>

### <span data-ttu-id="f446e-257">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="f446e-257">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="f446e-258">筆記</span><span class="sxs-lookup"><span data-stu-id="f446e-258">NOTES</span></span>

## <span data-ttu-id="f446e-259">相關連結</span><span class="sxs-lookup"><span data-stu-id="f446e-259">RELATED LINKS</span></span>

[<span data-ttu-id="f446e-260">AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="f446e-260">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="f446e-261">移除-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f446e-261">Remove-AzureRmKeyVaultAccessPolicy</span></span>](./Remove-AzureRmKeyVaultAccessPolicy.md)


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 3baa4a20d6109d2767dee1b4ff53e2b363adfccf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905957"
---
# <span data-ttu-id="38b28-101">Update-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="38b28-101">Update-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="38b28-102">簡介</span><span class="sxs-lookup"><span data-stu-id="38b28-102">SYNOPSIS</span></span>
<span data-ttu-id="38b28-103">將 Azure NetApp 檔案 (ANF) 目錄組配置更新為提供的選擇性修改程式。</span><span class="sxs-lookup"><span data-stu-id="38b28-103">Updates an Azure NetApp Files (ANF) active directory configuration to the optional modifiers provided.</span></span>

## <span data-ttu-id="38b28-104">語法</span><span class="sxs-lookup"><span data-stu-id="38b28-104">SYNTAX</span></span>

### <span data-ttu-id="38b28-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="38b28-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 -ActiveDirectoryId <String> [-Dns <String[]>] [-Domain <String>] [-Site <String>] [-SmbServerName <String>]
 [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>] [-KdcIP <String>]
 [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38b28-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="38b28-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesActiveDirectory -ActiveDirectoryId <String> [-Dns <String[]>] [-Domain <String>]
 [-Site <String>] [-SmbServerName <String>] [-Username <String>] [-Password <SecureString>]
 [-OrganizationalUnit <String>] [-KdcIP <String>] [-BackupOperator <String[]>]
 [-ServerRootCACertificate <String>] [-AdName <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38b28-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="38b28-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesActiveDirectory [-Dns <String[]>] [-Domain <String>] [-Site <String>]
 [-SmbServerName <String>] [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>]
 [-KdcIP <String>] [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 -InputObject <PSNetAppFilesActiveDirectory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38b28-108">描述</span><span class="sxs-lookup"><span data-stu-id="38b28-108">DESCRIPTION</span></span>
<span data-ttu-id="38b28-109">**Update-AzNetAppFilesAccount** Cmdlet 會修改 ANF Active Directory 組式。</span><span class="sxs-lookup"><span data-stu-id="38b28-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF active directory configuration.</span></span>

## <span data-ttu-id="38b28-110">例子</span><span class="sxs-lookup"><span data-stu-id="38b28-110">EXAMPLES</span></span>

### <span data-ttu-id="38b28-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="38b28-111">Example 1</span></span>
```powershell
PS C:\> Update-AzNetAppFilesActiveDirectory  -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyADName" -Username $adUsername
```

<span data-ttu-id="38b28-112">此命令會執行指定 Active Directory 組配置的更新，修改提供之使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="38b28-112">This command performs an update on the given active directory configuration modifying the username to that provided.</span></span>

## <span data-ttu-id="38b28-113">參數</span><span class="sxs-lookup"><span data-stu-id="38b28-113">PARAMETERS</span></span>

### <span data-ttu-id="38b28-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="38b28-114">-AccountName</span></span>
<span data-ttu-id="38b28-115">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="38b28-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b28-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="38b28-116">-AccountObject</span></span>
<span data-ttu-id="38b28-117">Active Directory 物件的帳戶</span><span class="sxs-lookup"><span data-stu-id="38b28-117">The account for the active directory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38b28-118">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="38b28-118">-ActiveDirectoryId</span></span>
<span data-ttu-id="38b28-119">ANF Active Directory 的識別碼</span><span class="sxs-lookup"><span data-stu-id="38b28-119">The ID of the ANF active directory</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b28-120">-AdName</span><span class="sxs-lookup"><span data-stu-id="38b28-120">-AdName</span></span>
<span data-ttu-id="38b28-121">Active Directory 電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="38b28-121">Name of the active directory machine.</span></span>
<span data-ttu-id="38b28-122">此選擇性參數只能在建立 kerberos 音量時使用</span><span class="sxs-lookup"><span data-stu-id="38b28-122">This optional parameter is used only while creating kerberos volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b28-123">-BackupOperator</span><span class="sxs-lookup"><span data-stu-id="38b28-123">-BackupOperator</span></span>
<span data-ttu-id="38b28-124">要新加入內建備份運算子 Active Directory 群組的使用者。</span><span class="sxs-lookup"><span data-stu-id="38b28-124">Users to be added to the Built-in Backup Operator active directory group.</span></span>
<span data-ttu-id="38b28-125">不含網域指定元的唯一使用者名稱清單</span><span class="sxs-lookup"><span data-stu-id="38b28-125">A list of unique usernames without domain specifier</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b28-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38b28-126">-DefaultProfile</span></span>
<span data-ttu-id="38b28-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="38b28-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38b28-128">-Dns</span><span class="sxs-lookup"><span data-stu-id="38b28-128">-Dns</span></span>
<span data-ttu-id="38b28-129">僅針對 Active Directory 網域 (IPv4 的 DNS 伺服器 IP 位址) 逗號分隔清單</span><span class="sxs-lookup"><span data-stu-id="38b28-129">Comma separated list of DNS server IP addresses (IPv4 only) for the Active Directory domain</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b28-130">-網域</span><span class="sxs-lookup"><span data-stu-id="38b28-130">-Domain</span></span>
<span data-ttu-id="38b28-131">Active Directory 網域的名稱</span><span class="sxs-lookup"><span data-stu-id="38b28-131">Name of the Active Directory domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b28-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38b28-132">-InputObject</span></span>
<span data-ttu-id="38b28-133">要移除的 Active Directory 物件</span><span class="sxs-lookup"><span data-stu-id="38b28-133">The active directory object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38b28-134">-KdcIP</span><span class="sxs-lookup"><span data-stu-id="38b28-134">-KdcIP</span></span>
<span data-ttu-id="38b28-135">Active Directory 電腦的伺服器 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="38b28-135">kdc server IP addresses for the active directory machine.</span></span>
<span data-ttu-id="38b28-136">只有在建立 kerberos 音量時，才使用這個選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="38b28-136">This optional parameter is used only while creating kerberos volume.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b28-137">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="38b28-137">-OrganizationalUnit</span></span>
<span data-ttu-id="38b28-138">Windows Active Directory (OU) 組織單位</span><span class="sxs-lookup"><span data-stu-id="38b28-138">The Organizational Unit (OU) within the Windows Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b28-139">-密碼</span><span class="sxs-lookup"><span data-stu-id="38b28-139">-Password</span></span>
<span data-ttu-id="38b28-140">Active Directory 網域系統管理員的純文字密碼，在回應中會遮罩值</span><span class="sxs-lookup"><span data-stu-id="38b28-140">Plain text password of Active Directory domain administrator, value is masked in the response</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b28-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38b28-141">-ResourceGroupName</span></span>
<span data-ttu-id="38b28-142">ANF 帳戶的資源群組</span><span class="sxs-lookup"><span data-stu-id="38b28-142">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b28-143">-ServerRootCACertificate</span><span class="sxs-lookup"><span data-stu-id="38b28-143">-ServerRootCACertificate</span></span>
<span data-ttu-id="38b28-144">啟用 SSL/TLS 上的 LDAP 時，LDAP 用戶端必須擁有 base64 編碼的 Active Directory 憑證服務的自我簽署根 CA 憑證，此選擇性參數僅適用于具有 LDAP 使用者地圖卷的雙通訊協定。</span><span class="sxs-lookup"><span data-stu-id="38b28-144">When LDAP over SSL/TLS is enabled, the LDAP client is required to have base64 encoded Active Directory Certificate Service's self-signed root CA certificate, this optional parameter is used only for dual protocol with LDAP user-mapping volumes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b28-145">-網站</span><span class="sxs-lookup"><span data-stu-id="38b28-145">-Site</span></span>
<span data-ttu-id="38b28-146">服務將限制網域控制站探索的 Active Directory 網站</span><span class="sxs-lookup"><span data-stu-id="38b28-146">The Active Directory site the service will limit Domain Controller discovery to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b28-147">-SmbServerName</span><span class="sxs-lookup"><span data-stu-id="38b28-147">-SmbServerName</span></span>
<span data-ttu-id="38b28-148">SMB 伺服器的 NetBIOS 名稱。</span><span class="sxs-lookup"><span data-stu-id="38b28-148">NetBIOS name of the SMB server.</span></span>
<span data-ttu-id="38b28-149">此名稱將在 AD 中註冊為電腦帳戶，並用來安裝大量</span><span class="sxs-lookup"><span data-stu-id="38b28-149">This name will be registered as a computer account in the AD and used to mount volumes</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b28-150">-使用者名稱</span><span class="sxs-lookup"><span data-stu-id="38b28-150">-Username</span></span>
<span data-ttu-id="38b28-151">Active Directory 網域系統管理員的使用者名稱</span><span class="sxs-lookup"><span data-stu-id="38b28-151">Username of Active Directory domain administrator</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38b28-152">-確認</span><span class="sxs-lookup"><span data-stu-id="38b28-152">-Confirm</span></span>
<span data-ttu-id="38b28-153">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="38b28-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38b28-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38b28-154">-WhatIf</span></span>
<span data-ttu-id="38b28-155">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="38b28-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38b28-156">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="38b28-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38b28-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38b28-157">CommonParameters</span></span>
<span data-ttu-id="38b28-158">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="38b28-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38b28-159">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38b28-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38b28-160">輸入</span><span class="sxs-lookup"><span data-stu-id="38b28-160">INPUTS</span></span>

### <span data-ttu-id="38b28-161">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="38b28-161">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="38b28-162">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="38b28-162">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="38b28-163">輸出</span><span class="sxs-lookup"><span data-stu-id="38b28-163">OUTPUTS</span></span>

### <span data-ttu-id="38b28-164">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="38b28-164">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="38b28-165">筆記</span><span class="sxs-lookup"><span data-stu-id="38b28-165">NOTES</span></span>

## <span data-ttu-id="38b28-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="38b28-166">RELATED LINKS</span></span>

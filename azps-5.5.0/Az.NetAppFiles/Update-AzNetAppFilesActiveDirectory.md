---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 1144108ce4338065183dc31b0f72dbb51dc69d19
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140562"
---
# <span data-ttu-id="20156-101">Update-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="20156-101">Update-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="20156-102">摘要</span><span class="sxs-lookup"><span data-stu-id="20156-102">SYNOPSIS</span></span>
<span data-ttu-id="20156-103">將 Azure NetApp 檔案 (ANF) active directory 設定更新為提供的選擇性修飾符。</span><span class="sxs-lookup"><span data-stu-id="20156-103">Updates an Azure NetApp Files (ANF) active directory configuration to the optional modifiers provided.</span></span>

## <span data-ttu-id="20156-104">句法</span><span class="sxs-lookup"><span data-stu-id="20156-104">SYNTAX</span></span>

### <span data-ttu-id="20156-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="20156-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String>
 -ActiveDirectoryId <String> [-Dns <String[]>] [-Domain <String>] [-Site <String>] [-SmbServerName <String>]
 [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>] [-KdcIP <String>]
 [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20156-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20156-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesActiveDirectory -ActiveDirectoryId <String> [-Dns <String[]>] [-Domain <String>]
 [-Site <String>] [-SmbServerName <String>] [-Username <String>] [-Password <SecureString>]
 [-OrganizationalUnit <String>] [-KdcIP <String>] [-BackupOperator <String[]>]
 [-ServerRootCACertificate <String>] [-AdName <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20156-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20156-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesActiveDirectory [-Dns <String[]>] [-Domain <String>] [-Site <String>]
 [-SmbServerName <String>] [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>]
 [-KdcIP <String>] [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 -InputObject <PSNetAppFilesActiveDirectory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="20156-108">說明</span><span class="sxs-lookup"><span data-stu-id="20156-108">DESCRIPTION</span></span>
<span data-ttu-id="20156-109">**AzNetAppFilesAccount** Cmdlet 會修改 ANF active directory 設定。</span><span class="sxs-lookup"><span data-stu-id="20156-109">The **Update-AzNetAppFilesAccount** cmdlet modifies an ANF active directory configuration.</span></span>

## <span data-ttu-id="20156-110">示例</span><span class="sxs-lookup"><span data-stu-id="20156-110">EXAMPLES</span></span>

### <span data-ttu-id="20156-111">範例1</span><span class="sxs-lookup"><span data-stu-id="20156-111">Example 1</span></span>
```powershell
PS C:\> Update-AzNetAppFilesActiveDirectory  -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MyADName" -Username $adUsername
```

<span data-ttu-id="20156-112">這個命令會在指定的 active directory 設定上執行更新，以修改所提供的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="20156-112">This command performs an update on the given active directory configuration modifying the username to that provided.</span></span>

## <span data-ttu-id="20156-113">參數</span><span class="sxs-lookup"><span data-stu-id="20156-113">PARAMETERS</span></span>

### <span data-ttu-id="20156-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="20156-114">-AccountName</span></span>
<span data-ttu-id="20156-115">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="20156-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="20156-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="20156-116">-AccountObject</span></span>
<span data-ttu-id="20156-117">Active directory 物件的帳戶</span><span class="sxs-lookup"><span data-stu-id="20156-117">The account for the active directory object</span></span>

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

### <span data-ttu-id="20156-118">-ActiveDirectoryId</span><span class="sxs-lookup"><span data-stu-id="20156-118">-ActiveDirectoryId</span></span>
<span data-ttu-id="20156-119">ANF active directory 的識別碼</span><span class="sxs-lookup"><span data-stu-id="20156-119">The ID of the ANF active directory</span></span>

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

### <span data-ttu-id="20156-120">-AdName</span><span class="sxs-lookup"><span data-stu-id="20156-120">-AdName</span></span>
<span data-ttu-id="20156-121">Active directory 電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="20156-121">Name of the active directory machine.</span></span>
<span data-ttu-id="20156-122">此選擇性參數只會在建立 kerberos 卷時使用</span><span class="sxs-lookup"><span data-stu-id="20156-122">This optional parameter is used only while creating kerberos volume</span></span>

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

### <span data-ttu-id="20156-123">-BackupOperator</span><span class="sxs-lookup"><span data-stu-id="20156-123">-BackupOperator</span></span>
<span data-ttu-id="20156-124">要新增至內建備份操作員 active directory 群組的使用者。</span><span class="sxs-lookup"><span data-stu-id="20156-124">Users to be added to the Built-in Backup Operator active directory group.</span></span>
<span data-ttu-id="20156-125">不含網域說明符的唯一使用者名清單</span><span class="sxs-lookup"><span data-stu-id="20156-125">A list of unique usernames without domain specifier</span></span>

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

### <span data-ttu-id="20156-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20156-126">-DefaultProfile</span></span>
<span data-ttu-id="20156-127">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="20156-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20156-128">-Dns</span><span class="sxs-lookup"><span data-stu-id="20156-128">-Dns</span></span>
<span data-ttu-id="20156-129">以逗號分隔的 DNS 伺服器 IP 位址清單 (適用于 Active Directory 網域的 IPv4) </span><span class="sxs-lookup"><span data-stu-id="20156-129">Comma separated list of DNS server IP addresses (IPv4 only) for the Active Directory domain</span></span>

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

### <span data-ttu-id="20156-130">-網域</span><span class="sxs-lookup"><span data-stu-id="20156-130">-Domain</span></span>
<span data-ttu-id="20156-131">Active Directory 網域的名稱</span><span class="sxs-lookup"><span data-stu-id="20156-131">Name of the Active Directory domain</span></span>

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

### <span data-ttu-id="20156-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20156-132">-InputObject</span></span>
<span data-ttu-id="20156-133">要移除的 active directory 物件</span><span class="sxs-lookup"><span data-stu-id="20156-133">The active directory object to remove</span></span>

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

### <span data-ttu-id="20156-134">-KdcIP</span><span class="sxs-lookup"><span data-stu-id="20156-134">-KdcIP</span></span>
<span data-ttu-id="20156-135">active directory 電腦的 kdc 伺服器 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="20156-135">kdc server IP addresses for the active directory machine.</span></span>
<span data-ttu-id="20156-136">此選擇性參數只會在建立 kerberos 卷時使用。</span><span class="sxs-lookup"><span data-stu-id="20156-136">This optional parameter is used only while creating kerberos volume.</span></span>

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

### <span data-ttu-id="20156-137">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="20156-137">-OrganizationalUnit</span></span>
<span data-ttu-id="20156-138">在 Windows Active Directory 中) 組織單位 (OU</span><span class="sxs-lookup"><span data-stu-id="20156-138">The Organizational Unit (OU) within the Windows Active Directory</span></span>

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

### <span data-ttu-id="20156-139">-Password</span><span class="sxs-lookup"><span data-stu-id="20156-139">-Password</span></span>
<span data-ttu-id="20156-140">Active Directory 網域系統管理員的純文字密碼，回應中的值會遮罩</span><span class="sxs-lookup"><span data-stu-id="20156-140">Plain text password of Active Directory domain administrator, value is masked in the response</span></span>

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

### <span data-ttu-id="20156-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20156-141">-ResourceGroupName</span></span>
<span data-ttu-id="20156-142">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="20156-142">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="20156-143">-ServerRootCACertificate</span><span class="sxs-lookup"><span data-stu-id="20156-143">-ServerRootCACertificate</span></span>
<span data-ttu-id="20156-144">當啟用 [SSL/TLS 的 LDAP] 時，必須使用 LDAP 用戶端才能使用 base64 編碼的 Active Directory 憑證服務的自我簽署根 CA 憑證，此選擇性參數只適用于具有 LDAP 使用者對應卷的雙通訊協定。</span><span class="sxs-lookup"><span data-stu-id="20156-144">When LDAP over SSL/TLS is enabled, the LDAP client is required to have base64 encoded Active Directory Certificate Service's self-signed root CA certificate, this optional parameter is used only for dual protocol with LDAP user-mapping volumes.</span></span>

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

### <span data-ttu-id="20156-145">-網站</span><span class="sxs-lookup"><span data-stu-id="20156-145">-Site</span></span>
<span data-ttu-id="20156-146">Active Directory 網站服務會將網網域控制站探索限制在</span><span class="sxs-lookup"><span data-stu-id="20156-146">The Active Directory site the service will limit Domain Controller discovery to</span></span>

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

### <span data-ttu-id="20156-147">-SmbServerName</span><span class="sxs-lookup"><span data-stu-id="20156-147">-SmbServerName</span></span>
<span data-ttu-id="20156-148">SMB 伺服器的 NetBIOS 名稱。</span><span class="sxs-lookup"><span data-stu-id="20156-148">NetBIOS name of the SMB server.</span></span>
<span data-ttu-id="20156-149">此名稱將在 AD 中註冊為電腦帳戶，並用於裝入磁片卷</span><span class="sxs-lookup"><span data-stu-id="20156-149">This name will be registered as a computer account in the AD and used to mount volumes</span></span>

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

### <span data-ttu-id="20156-150">-Username</span><span class="sxs-lookup"><span data-stu-id="20156-150">-Username</span></span>
<span data-ttu-id="20156-151">Active Directory 網域系統管理員的使用者名稱</span><span class="sxs-lookup"><span data-stu-id="20156-151">Username of Active Directory domain administrator</span></span>

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

### <span data-ttu-id="20156-152">-確認</span><span class="sxs-lookup"><span data-stu-id="20156-152">-Confirm</span></span>
<span data-ttu-id="20156-153">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="20156-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20156-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20156-154">-WhatIf</span></span>
<span data-ttu-id="20156-155">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="20156-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20156-156">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="20156-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20156-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20156-157">CommonParameters</span></span>
<span data-ttu-id="20156-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="20156-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20156-159">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="20156-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20156-160">輸入</span><span class="sxs-lookup"><span data-stu-id="20156-160">INPUTS</span></span>

### <span data-ttu-id="20156-161">PSNetAppFilesAccount 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="20156-161">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="20156-162">PSNetAppFilesActiveDirectory 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="20156-162">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="20156-163">輸出</span><span class="sxs-lookup"><span data-stu-id="20156-163">OUTPUTS</span></span>

### <span data-ttu-id="20156-164">PSNetAppFilesActiveDirectory 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="20156-164">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="20156-165">筆記</span><span class="sxs-lookup"><span data-stu-id="20156-165">NOTES</span></span>

## <span data-ttu-id="20156-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="20156-166">RELATED LINKS</span></span>

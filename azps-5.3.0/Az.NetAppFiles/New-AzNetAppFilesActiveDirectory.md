---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 9ce36109d0ee7be1c0a513db06a81fb61b926697
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435245"
---
# <span data-ttu-id="1964b-101">New-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="1964b-101">New-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="1964b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1964b-102">SYNOPSIS</span></span>
<span data-ttu-id="1964b-103"> (ANF) active directory 設定中建立新的 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="1964b-103">Creates a new Azure NetApp Files (ANF) active directory configuration.</span></span>

## <span data-ttu-id="1964b-104">句法</span><span class="sxs-lookup"><span data-stu-id="1964b-104">SYNTAX</span></span>

### <span data-ttu-id="1964b-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1964b-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String> [-Dns <String[]>]
 -Domain <String> [-Site <String>] -SmbServerName <String> [-Username <String>] [-Password <SecureString>]
 [-OrganizationalUnit <String>] [-KdcIP <String>] [-BackupOperator <String[]>]
 [-ServerRootCACertificate <String>] [-AdName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1964b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1964b-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesActiveDirectory [-Dns <String[]>] -Domain <String> [-Site <String>] -SmbServerName <String>
 [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>] [-KdcIP <String>]
 [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1964b-107">說明</span><span class="sxs-lookup"><span data-stu-id="1964b-107">DESCRIPTION</span></span>
<span data-ttu-id="1964b-108">**新的-AzNetAppFilesActiveDirectory** Cmdlet 會為 ANF 帳戶建立新的 active directory 設定。</span><span class="sxs-lookup"><span data-stu-id="1964b-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new active directory configuration for an ANF account.</span></span>

## <span data-ttu-id="1964b-109">示例</span><span class="sxs-lookup"><span data-stu-id="1964b-109">EXAMPLES</span></span>

### <span data-ttu-id="1964b-110">範例1</span><span class="sxs-lookup"><span data-stu-id="1964b-110">Example 1</span></span>
```powershell
PS C:\> $pwd_secure_string = Read-Host "Enter a Password" -AsSecureString
PS C:\> New-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MyADName" -Username "AdUserName -Password $pwd_secure_string -Domain "AdDomain" -Dns "192.0.2.2" -SmbServerName "AdSmbServerName"
```

<span data-ttu-id="1964b-111">這個命令會從 promt 中取得 AD 密碼，以 secreates ANF 帳戶 "MyAnfAccount" 的新 Active Directory 設定。</span><span class="sxs-lookup"><span data-stu-id="1964b-111">This command gets the AD password from promt into a secreates the new Active Directory configuration for the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="1964b-112">參數</span><span class="sxs-lookup"><span data-stu-id="1964b-112">PARAMETERS</span></span>

### <span data-ttu-id="1964b-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1964b-113">-AccountName</span></span>
<span data-ttu-id="1964b-114">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="1964b-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="1964b-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="1964b-115">-AccountObject</span></span>
<span data-ttu-id="1964b-116">新備份策略物件的帳戶</span><span class="sxs-lookup"><span data-stu-id="1964b-116">The Account for the new Backup Policy object</span></span>

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

### <span data-ttu-id="1964b-117">-AdName</span><span class="sxs-lookup"><span data-stu-id="1964b-117">-AdName</span></span>
<span data-ttu-id="1964b-118">Active directory 電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="1964b-118">Name of the active directory machine.</span></span>
<span data-ttu-id="1964b-119">此選擇性參數只會在建立 kerberos 卷時使用</span><span class="sxs-lookup"><span data-stu-id="1964b-119">This optional parameter is used only while creating kerberos volume</span></span>

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

### <span data-ttu-id="1964b-120">-BackupOperator</span><span class="sxs-lookup"><span data-stu-id="1964b-120">-BackupOperator</span></span>
<span data-ttu-id="1964b-121">要新增至內建備份操作員 active directory 群組的使用者。</span><span class="sxs-lookup"><span data-stu-id="1964b-121">Users to be added to the Built-in Backup Operator active directory group.</span></span>
<span data-ttu-id="1964b-122">不含網域說明符的唯一使用者名清單</span><span class="sxs-lookup"><span data-stu-id="1964b-122">A list of unique usernames without domain specifier</span></span>

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

### <span data-ttu-id="1964b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1964b-123">-DefaultProfile</span></span>
<span data-ttu-id="1964b-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1964b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1964b-125">-Dns</span><span class="sxs-lookup"><span data-stu-id="1964b-125">-Dns</span></span>
<span data-ttu-id="1964b-126">以逗號分隔的 DNS 伺服器 IP 位址清單 (適用于 Active Directory 網域的 IPv4) </span><span class="sxs-lookup"><span data-stu-id="1964b-126">Comma separated list of DNS server IP addresses (IPv4 only) for the Active Directory domain</span></span>

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

### <span data-ttu-id="1964b-127">-網域</span><span class="sxs-lookup"><span data-stu-id="1964b-127">-Domain</span></span>
<span data-ttu-id="1964b-128">Active Directory 網域的名稱</span><span class="sxs-lookup"><span data-stu-id="1964b-128">Name of the Active Directory domain</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1964b-129">-KdcIP</span><span class="sxs-lookup"><span data-stu-id="1964b-129">-KdcIP</span></span>
<span data-ttu-id="1964b-130">active directory 電腦的 kdc 伺服器 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="1964b-130">kdc server IP addresses for the active directory machine.</span></span>
<span data-ttu-id="1964b-131">此選擇性參數只會在建立 kerberos 卷時使用。</span><span class="sxs-lookup"><span data-stu-id="1964b-131">This optional parameter is used only while creating kerberos volume.</span></span>

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

### <span data-ttu-id="1964b-132">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="1964b-132">-OrganizationalUnit</span></span>
<span data-ttu-id="1964b-133">在 Windows Active Directory 中) 組織單位 (OU</span><span class="sxs-lookup"><span data-stu-id="1964b-133">The Organizational Unit (OU) within the Windows Active Directory</span></span>

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

### <span data-ttu-id="1964b-134">-Password</span><span class="sxs-lookup"><span data-stu-id="1964b-134">-Password</span></span>
<span data-ttu-id="1964b-135">Active Directory 網域系統管理員的純文字密碼，回應中的值會遮罩</span><span class="sxs-lookup"><span data-stu-id="1964b-135">Plain text password of Active Directory domain administrator, value is masked in the response</span></span>

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

### <span data-ttu-id="1964b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1964b-136">-ResourceGroupName</span></span>
<span data-ttu-id="1964b-137">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="1964b-137">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="1964b-138">-ServerRootCACertificate</span><span class="sxs-lookup"><span data-stu-id="1964b-138">-ServerRootCACertificate</span></span>
<span data-ttu-id="1964b-139">當啟用 [SSL/TLS 的 LDAP] 時，必須使用 LDAP 用戶端才能使用 base64 編碼的 Active Directory 憑證服務的自我簽署根 CA 憑證，此選擇性參數只適用于具有 LDAP 使用者對應卷的雙通訊協定。</span><span class="sxs-lookup"><span data-stu-id="1964b-139">When LDAP over SSL/TLS is enabled, the LDAP client is required to have base64 encoded Active Directory Certificate Service's self-signed root CA certificate, this optional parameter is used only for dual protocol with LDAP user-mapping volumes.</span></span>

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

### <span data-ttu-id="1964b-140">-網站</span><span class="sxs-lookup"><span data-stu-id="1964b-140">-Site</span></span>
<span data-ttu-id="1964b-141">Active Directory 網站服務會將網網域控制站探索限制在</span><span class="sxs-lookup"><span data-stu-id="1964b-141">The Active Directory site the service will limit Domain Controller discovery to</span></span>

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

### <span data-ttu-id="1964b-142">-SmbServerName</span><span class="sxs-lookup"><span data-stu-id="1964b-142">-SmbServerName</span></span>
<span data-ttu-id="1964b-143">SMB 伺服器的 NetBIOS 名稱。</span><span class="sxs-lookup"><span data-stu-id="1964b-143">NetBIOS name of the SMB server.</span></span>
<span data-ttu-id="1964b-144">此名稱將在 AD 中註冊為電腦帳戶，並用於裝入磁片卷</span><span class="sxs-lookup"><span data-stu-id="1964b-144">This name will be registered as a computer account in the AD and used to mount volumes</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1964b-145">-Username</span><span class="sxs-lookup"><span data-stu-id="1964b-145">-Username</span></span>
<span data-ttu-id="1964b-146">Active Directory 網域系統管理員的使用者名稱</span><span class="sxs-lookup"><span data-stu-id="1964b-146">Username of Active Directory domain administrator</span></span>

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

### <span data-ttu-id="1964b-147">-確認</span><span class="sxs-lookup"><span data-stu-id="1964b-147">-Confirm</span></span>
<span data-ttu-id="1964b-148">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1964b-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1964b-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1964b-149">-WhatIf</span></span>
<span data-ttu-id="1964b-150">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1964b-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1964b-151">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1964b-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1964b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1964b-152">CommonParameters</span></span>
<span data-ttu-id="1964b-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1964b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1964b-154">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1964b-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1964b-155">輸入</span><span class="sxs-lookup"><span data-stu-id="1964b-155">INPUTS</span></span>

### <span data-ttu-id="1964b-156">PSNetAppFilesAccount 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="1964b-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="1964b-157">輸出</span><span class="sxs-lookup"><span data-stu-id="1964b-157">OUTPUTS</span></span>

### <span data-ttu-id="1964b-158">PSNetAppFilesActiveDirectory 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="1964b-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="1964b-159">筆記</span><span class="sxs-lookup"><span data-stu-id="1964b-159">NOTES</span></span>

## <span data-ttu-id="1964b-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="1964b-160">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 9ce36109d0ee7be1c0a513db06a81fb61b926697
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281770"
---
# <span data-ttu-id="a4eca-101">New-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="a4eca-101">New-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="a4eca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a4eca-102">SYNOPSIS</span></span>
<span data-ttu-id="a4eca-103"> (ANF) active directory 設定中建立新的 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="a4eca-103">Creates a new Azure NetApp Files (ANF) active directory configuration.</span></span>

## <span data-ttu-id="a4eca-104">句法</span><span class="sxs-lookup"><span data-stu-id="a4eca-104">SYNTAX</span></span>

### <span data-ttu-id="a4eca-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a4eca-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String> [-Dns <String[]>]
 -Domain <String> [-Site <String>] -SmbServerName <String> [-Username <String>] [-Password <SecureString>]
 [-OrganizationalUnit <String>] [-KdcIP <String>] [-BackupOperator <String[]>]
 [-ServerRootCACertificate <String>] [-AdName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4eca-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4eca-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesActiveDirectory [-Dns <String[]>] -Domain <String> [-Site <String>] -SmbServerName <String>
 [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>] [-KdcIP <String>]
 [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a4eca-107">說明</span><span class="sxs-lookup"><span data-stu-id="a4eca-107">DESCRIPTION</span></span>
<span data-ttu-id="a4eca-108">**新的-AzNetAppFilesActiveDirectory** Cmdlet 會為 ANF 帳戶建立新的 active directory 設定。</span><span class="sxs-lookup"><span data-stu-id="a4eca-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new active directory configuration for an ANF account.</span></span>

## <span data-ttu-id="a4eca-109">示例</span><span class="sxs-lookup"><span data-stu-id="a4eca-109">EXAMPLES</span></span>

### <span data-ttu-id="a4eca-110">範例1</span><span class="sxs-lookup"><span data-stu-id="a4eca-110">Example 1</span></span>
```powershell
PS C:\> $pwd_secure_string = Read-Host "Enter a Password" -AsSecureString
PS C:\> New-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MyADName" -Username "AdUserName -Password $pwd_secure_string -Domain "AdDomain" -Dns "192.0.2.2" -SmbServerName "AdSmbServerName"
```

<span data-ttu-id="a4eca-111">這個命令會從 promt 中取得 AD 密碼，以 secreates ANF 帳戶 "MyAnfAccount" 的新 Active Directory 設定。</span><span class="sxs-lookup"><span data-stu-id="a4eca-111">This command gets the AD password from promt into a secreates the new Active Directory configuration for the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="a4eca-112">參數</span><span class="sxs-lookup"><span data-stu-id="a4eca-112">PARAMETERS</span></span>

### <span data-ttu-id="a4eca-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a4eca-113">-AccountName</span></span>
<span data-ttu-id="a4eca-114">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="a4eca-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="a4eca-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="a4eca-115">-AccountObject</span></span>
<span data-ttu-id="a4eca-116">新備份策略物件的帳戶</span><span class="sxs-lookup"><span data-stu-id="a4eca-116">The Account for the new Backup Policy object</span></span>

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

### <span data-ttu-id="a4eca-117">-AdName</span><span class="sxs-lookup"><span data-stu-id="a4eca-117">-AdName</span></span>
<span data-ttu-id="a4eca-118">Active directory 電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="a4eca-118">Name of the active directory machine.</span></span>
<span data-ttu-id="a4eca-119">此選擇性參數只會在建立 kerberos 卷時使用</span><span class="sxs-lookup"><span data-stu-id="a4eca-119">This optional parameter is used only while creating kerberos volume</span></span>

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

### <span data-ttu-id="a4eca-120">-BackupOperator</span><span class="sxs-lookup"><span data-stu-id="a4eca-120">-BackupOperator</span></span>
<span data-ttu-id="a4eca-121">要新增至內建備份操作員 active directory 群組的使用者。</span><span class="sxs-lookup"><span data-stu-id="a4eca-121">Users to be added to the Built-in Backup Operator active directory group.</span></span>
<span data-ttu-id="a4eca-122">不含網域說明符的唯一使用者名清單</span><span class="sxs-lookup"><span data-stu-id="a4eca-122">A list of unique usernames without domain specifier</span></span>

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

### <span data-ttu-id="a4eca-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4eca-123">-DefaultProfile</span></span>
<span data-ttu-id="a4eca-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a4eca-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4eca-125">-Dns</span><span class="sxs-lookup"><span data-stu-id="a4eca-125">-Dns</span></span>
<span data-ttu-id="a4eca-126">以逗號分隔的 DNS 伺服器 IP 位址清單 (適用于 Active Directory 網域的 IPv4) </span><span class="sxs-lookup"><span data-stu-id="a4eca-126">Comma separated list of DNS server IP addresses (IPv4 only) for the Active Directory domain</span></span>

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

### <span data-ttu-id="a4eca-127">-網域</span><span class="sxs-lookup"><span data-stu-id="a4eca-127">-Domain</span></span>
<span data-ttu-id="a4eca-128">Active Directory 網域的名稱</span><span class="sxs-lookup"><span data-stu-id="a4eca-128">Name of the Active Directory domain</span></span>

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

### <span data-ttu-id="a4eca-129">-KdcIP</span><span class="sxs-lookup"><span data-stu-id="a4eca-129">-KdcIP</span></span>
<span data-ttu-id="a4eca-130">active directory 電腦的 kdc 伺服器 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="a4eca-130">kdc server IP addresses for the active directory machine.</span></span>
<span data-ttu-id="a4eca-131">此選擇性參數只會在建立 kerberos 卷時使用。</span><span class="sxs-lookup"><span data-stu-id="a4eca-131">This optional parameter is used only while creating kerberos volume.</span></span>

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

### <span data-ttu-id="a4eca-132">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="a4eca-132">-OrganizationalUnit</span></span>
<span data-ttu-id="a4eca-133">在 Windows Active Directory 中) 組織單位 (OU</span><span class="sxs-lookup"><span data-stu-id="a4eca-133">The Organizational Unit (OU) within the Windows Active Directory</span></span>

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

### <span data-ttu-id="a4eca-134">-Password</span><span class="sxs-lookup"><span data-stu-id="a4eca-134">-Password</span></span>
<span data-ttu-id="a4eca-135">Active Directory 網域系統管理員的純文字密碼，回應中的值會遮罩</span><span class="sxs-lookup"><span data-stu-id="a4eca-135">Plain text password of Active Directory domain administrator, value is masked in the response</span></span>

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

### <span data-ttu-id="a4eca-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4eca-136">-ResourceGroupName</span></span>
<span data-ttu-id="a4eca-137">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="a4eca-137">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="a4eca-138">-ServerRootCACertificate</span><span class="sxs-lookup"><span data-stu-id="a4eca-138">-ServerRootCACertificate</span></span>
<span data-ttu-id="a4eca-139">當啟用 [SSL/TLS 的 LDAP] 時，必須使用 LDAP 用戶端才能使用 base64 編碼的 Active Directory 憑證服務的自我簽署根 CA 憑證，此選擇性參數只適用于具有 LDAP 使用者對應卷的雙通訊協定。</span><span class="sxs-lookup"><span data-stu-id="a4eca-139">When LDAP over SSL/TLS is enabled, the LDAP client is required to have base64 encoded Active Directory Certificate Service's self-signed root CA certificate, this optional parameter is used only for dual protocol with LDAP user-mapping volumes.</span></span>

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

### <span data-ttu-id="a4eca-140">-網站</span><span class="sxs-lookup"><span data-stu-id="a4eca-140">-Site</span></span>
<span data-ttu-id="a4eca-141">Active Directory 網站服務會將網網域控制站探索限制在</span><span class="sxs-lookup"><span data-stu-id="a4eca-141">The Active Directory site the service will limit Domain Controller discovery to</span></span>

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

### <span data-ttu-id="a4eca-142">-SmbServerName</span><span class="sxs-lookup"><span data-stu-id="a4eca-142">-SmbServerName</span></span>
<span data-ttu-id="a4eca-143">SMB 伺服器的 NetBIOS 名稱。</span><span class="sxs-lookup"><span data-stu-id="a4eca-143">NetBIOS name of the SMB server.</span></span>
<span data-ttu-id="a4eca-144">此名稱將在 AD 中註冊為電腦帳戶，並用於裝入磁片卷</span><span class="sxs-lookup"><span data-stu-id="a4eca-144">This name will be registered as a computer account in the AD and used to mount volumes</span></span>

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

### <span data-ttu-id="a4eca-145">-Username</span><span class="sxs-lookup"><span data-stu-id="a4eca-145">-Username</span></span>
<span data-ttu-id="a4eca-146">Active Directory 網域系統管理員的使用者名稱</span><span class="sxs-lookup"><span data-stu-id="a4eca-146">Username of Active Directory domain administrator</span></span>

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

### <span data-ttu-id="a4eca-147">-確認</span><span class="sxs-lookup"><span data-stu-id="a4eca-147">-Confirm</span></span>
<span data-ttu-id="a4eca-148">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a4eca-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4eca-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4eca-149">-WhatIf</span></span>
<span data-ttu-id="a4eca-150">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a4eca-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4eca-151">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a4eca-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4eca-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4eca-152">CommonParameters</span></span>
<span data-ttu-id="a4eca-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a4eca-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4eca-154">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a4eca-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4eca-155">輸入</span><span class="sxs-lookup"><span data-stu-id="a4eca-155">INPUTS</span></span>

### <span data-ttu-id="a4eca-156">PSNetAppFilesAccount 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="a4eca-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="a4eca-157">輸出</span><span class="sxs-lookup"><span data-stu-id="a4eca-157">OUTPUTS</span></span>

### <span data-ttu-id="a4eca-158">PSNetAppFilesActiveDirectory 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="a4eca-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="a4eca-159">筆記</span><span class="sxs-lookup"><span data-stu-id="a4eca-159">NOTES</span></span>

## <span data-ttu-id="a4eca-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="a4eca-160">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/new-aznetappfilesactivedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesActiveDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesActiveDirectory.md
ms.openlocfilehash: 73d0ae2a4f4595024db3ee5553a446a5832f0476
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906045"
---
# <span data-ttu-id="a473d-101">New-AzNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="a473d-101">New-AzNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="a473d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a473d-102">SYNOPSIS</span></span>
<span data-ttu-id="a473d-103">在 ACTIVE 目錄組 (ANF 中) Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="a473d-103">Creates a new Azure NetApp Files (ANF) active directory configuration.</span></span>

## <span data-ttu-id="a473d-104">語法</span><span class="sxs-lookup"><span data-stu-id="a473d-104">SYNTAX</span></span>

### <span data-ttu-id="a473d-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a473d-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesActiveDirectory -ResourceGroupName <String> -AccountName <String> [-Dns <String[]>]
 -Domain <String> [-Site <String>] -SmbServerName <String> [-Username <String>] [-Password <SecureString>]
 [-OrganizationalUnit <String>] [-KdcIP <String>] [-BackupOperator <String[]>]
 [-ServerRootCACertificate <String>] [-AdName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a473d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a473d-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesActiveDirectory [-Dns <String[]>] -Domain <String> [-Site <String>] -SmbServerName <String>
 [-Username <String>] [-Password <SecureString>] [-OrganizationalUnit <String>] [-KdcIP <String>]
 [-BackupOperator <String[]>] [-ServerRootCACertificate <String>] [-AdName <String>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a473d-107">描述</span><span class="sxs-lookup"><span data-stu-id="a473d-107">DESCRIPTION</span></span>
<span data-ttu-id="a473d-108">**New-AzNetAppFilesActiveDirectory** Cmdlet 會為 ANF 帳戶建立新的 Active Directory 組式。</span><span class="sxs-lookup"><span data-stu-id="a473d-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new active directory configuration for an ANF account.</span></span>

## <span data-ttu-id="a473d-109">例子</span><span class="sxs-lookup"><span data-stu-id="a473d-109">EXAMPLES</span></span>

### <span data-ttu-id="a473d-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="a473d-110">Example 1</span></span>
```powershell
PS C:\> $pwd_secure_string = Read-Host "Enter a Password" -AsSecureString
PS C:\> New-AzNetAppFilesActiveDirectory -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MyADName" -Username "AdUserName -Password $pwd_secure_string -Domain "AdDomain" -Dns "192.0.2.2" -SmbServerName "AdSmbServerName"
```

<span data-ttu-id="a473d-111">此命令會從 promt 將 AD 密碼變成一種預設，為 ANF 帳戶 「MyAnfAccount」的新 Active Directory 群組原則。</span><span class="sxs-lookup"><span data-stu-id="a473d-111">This command gets the AD password from promt into a secreates the new Active Directory configuration for the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="a473d-112">參數</span><span class="sxs-lookup"><span data-stu-id="a473d-112">PARAMETERS</span></span>

### <span data-ttu-id="a473d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a473d-113">-AccountName</span></span>
<span data-ttu-id="a473d-114">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="a473d-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="a473d-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="a473d-115">-AccountObject</span></span>
<span data-ttu-id="a473d-116">新備份策略物件的帳戶</span><span class="sxs-lookup"><span data-stu-id="a473d-116">The Account for the new Backup Policy object</span></span>

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

### <span data-ttu-id="a473d-117">-AdName</span><span class="sxs-lookup"><span data-stu-id="a473d-117">-AdName</span></span>
<span data-ttu-id="a473d-118">Active Directory 電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="a473d-118">Name of the active directory machine.</span></span>
<span data-ttu-id="a473d-119">此選擇性參數只能在建立 kerberos 音量時使用</span><span class="sxs-lookup"><span data-stu-id="a473d-119">This optional parameter is used only while creating kerberos volume</span></span>

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

### <span data-ttu-id="a473d-120">-BackupOperator</span><span class="sxs-lookup"><span data-stu-id="a473d-120">-BackupOperator</span></span>
<span data-ttu-id="a473d-121">要新加入內建備份運算子 Active Directory 群組的使用者。</span><span class="sxs-lookup"><span data-stu-id="a473d-121">Users to be added to the Built-in Backup Operator active directory group.</span></span>
<span data-ttu-id="a473d-122">不含網域指定元的唯一使用者名稱清單</span><span class="sxs-lookup"><span data-stu-id="a473d-122">A list of unique usernames without domain specifier</span></span>

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

### <span data-ttu-id="a473d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a473d-123">-DefaultProfile</span></span>
<span data-ttu-id="a473d-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a473d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a473d-125">-Dns</span><span class="sxs-lookup"><span data-stu-id="a473d-125">-Dns</span></span>
<span data-ttu-id="a473d-126">僅針對 Active Directory 網域 (IPv4 的 DNS 伺服器 IP 位址) 逗號分隔清單</span><span class="sxs-lookup"><span data-stu-id="a473d-126">Comma separated list of DNS server IP addresses (IPv4 only) for the Active Directory domain</span></span>

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

### <span data-ttu-id="a473d-127">-網域</span><span class="sxs-lookup"><span data-stu-id="a473d-127">-Domain</span></span>
<span data-ttu-id="a473d-128">Active Directory 網域的名稱</span><span class="sxs-lookup"><span data-stu-id="a473d-128">Name of the Active Directory domain</span></span>

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

### <span data-ttu-id="a473d-129">-KdcIP</span><span class="sxs-lookup"><span data-stu-id="a473d-129">-KdcIP</span></span>
<span data-ttu-id="a473d-130">Active Directory 電腦的伺服器 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="a473d-130">kdc server IP addresses for the active directory machine.</span></span>
<span data-ttu-id="a473d-131">只有在建立 kerberos 音量時，才使用這個選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="a473d-131">This optional parameter is used only while creating kerberos volume.</span></span>

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

### <span data-ttu-id="a473d-132">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="a473d-132">-OrganizationalUnit</span></span>
<span data-ttu-id="a473d-133">Windows Active Directory (OU) 組織單位</span><span class="sxs-lookup"><span data-stu-id="a473d-133">The Organizational Unit (OU) within the Windows Active Directory</span></span>

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

### <span data-ttu-id="a473d-134">-密碼</span><span class="sxs-lookup"><span data-stu-id="a473d-134">-Password</span></span>
<span data-ttu-id="a473d-135">Active Directory 網域系統管理員的純文字密碼，在回應中會遮罩值</span><span class="sxs-lookup"><span data-stu-id="a473d-135">Plain text password of Active Directory domain administrator, value is masked in the response</span></span>

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

### <span data-ttu-id="a473d-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a473d-136">-ResourceGroupName</span></span>
<span data-ttu-id="a473d-137">ANF 帳戶的資源群組</span><span class="sxs-lookup"><span data-stu-id="a473d-137">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="a473d-138">-ServerRootCACertificate</span><span class="sxs-lookup"><span data-stu-id="a473d-138">-ServerRootCACertificate</span></span>
<span data-ttu-id="a473d-139">啟用 SSL/TLS 上的 LDAP 時，LDAP 用戶端必須擁有 base64 編碼的 Active Directory 憑證服務的自我簽署根 CA 憑證，此選擇性參數僅適用于具有 LDAP 使用者地圖卷的雙通訊協定。</span><span class="sxs-lookup"><span data-stu-id="a473d-139">When LDAP over SSL/TLS is enabled, the LDAP client is required to have base64 encoded Active Directory Certificate Service's self-signed root CA certificate, this optional parameter is used only for dual protocol with LDAP user-mapping volumes.</span></span>

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

### <span data-ttu-id="a473d-140">-網站</span><span class="sxs-lookup"><span data-stu-id="a473d-140">-Site</span></span>
<span data-ttu-id="a473d-141">服務將限制網域控制站探索的 Active Directory 網站</span><span class="sxs-lookup"><span data-stu-id="a473d-141">The Active Directory site the service will limit Domain Controller discovery to</span></span>

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

### <span data-ttu-id="a473d-142">-SmbServerName</span><span class="sxs-lookup"><span data-stu-id="a473d-142">-SmbServerName</span></span>
<span data-ttu-id="a473d-143">SMB 伺服器的 NetBIOS 名稱。</span><span class="sxs-lookup"><span data-stu-id="a473d-143">NetBIOS name of the SMB server.</span></span>
<span data-ttu-id="a473d-144">此名稱將在 AD 中註冊為電腦帳戶，並用來安裝大量</span><span class="sxs-lookup"><span data-stu-id="a473d-144">This name will be registered as a computer account in the AD and used to mount volumes</span></span>

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

### <span data-ttu-id="a473d-145">-使用者名稱</span><span class="sxs-lookup"><span data-stu-id="a473d-145">-Username</span></span>
<span data-ttu-id="a473d-146">Active Directory 網域系統管理員的使用者名稱</span><span class="sxs-lookup"><span data-stu-id="a473d-146">Username of Active Directory domain administrator</span></span>

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

### <span data-ttu-id="a473d-147">-確認</span><span class="sxs-lookup"><span data-stu-id="a473d-147">-Confirm</span></span>
<span data-ttu-id="a473d-148">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a473d-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a473d-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a473d-149">-WhatIf</span></span>
<span data-ttu-id="a473d-150">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a473d-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a473d-151">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a473d-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a473d-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a473d-152">CommonParameters</span></span>
<span data-ttu-id="a473d-153">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a473d-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a473d-154">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a473d-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a473d-155">輸入</span><span class="sxs-lookup"><span data-stu-id="a473d-155">INPUTS</span></span>

### <span data-ttu-id="a473d-156">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="a473d-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="a473d-157">輸出</span><span class="sxs-lookup"><span data-stu-id="a473d-157">OUTPUTS</span></span>

### <span data-ttu-id="a473d-158">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="a473d-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesActiveDirectory</span></span>

## <span data-ttu-id="a473d-159">筆記</span><span class="sxs-lookup"><span data-stu-id="a473d-159">NOTES</span></span>

## <span data-ttu-id="a473d-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="a473d-160">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: ab02a118eab993174261fc1a70c2dedbd6403d5a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956538"
---
# <span data-ttu-id="d792a-101">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d792a-101">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="d792a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d792a-102">SYNOPSIS</span></span>
<span data-ttu-id="d792a-103">在 Data Lake Analytics 中修改目錄或目錄專案的 ACL 中的專案。</span><span class="sxs-lookup"><span data-stu-id="d792a-103">Modifies an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="d792a-104">句法</span><span class="sxs-lookup"><span data-stu-id="d792a-104">SYNTAX</span></span>

### <span data-ttu-id="d792a-105">SetCatalogAclEntryForUser (預設) </span><span class="sxs-lookup"><span data-stu-id="d792a-105">SetCatalogAclEntryForUser (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d792a-106">SetCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="d792a-106">SetCatalogItemAclEntryForUser</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d792a-107">SetCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="d792a-107">SetCatalogAclEntryForGroup</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d792a-108">SetCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="d792a-108">SetCatalogItemAclEntryForGroup</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d792a-109">SetCatalogAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="d792a-109">SetCatalogAclEntryForOther</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d792a-110">SetCatalogItemAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="d792a-110">SetCatalogItemAclEntryForOther</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d792a-111">SetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="d792a-111">SetCatalogAclEntryForUserOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d792a-112">SetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="d792a-112">SetCatalogItemAclEntryForUserOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d792a-113">SetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="d792a-113">SetCatalogAclEntryForGroupOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d792a-114">SetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="d792a-114">SetCatalogItemAclEntryForGroupOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d792a-115">說明</span><span class="sxs-lookup"><span data-stu-id="d792a-115">DESCRIPTION</span></span>
<span data-ttu-id="d792a-116">**AzDataLakeAnalyticsCatalogItemAclEntry** Cmdlet 會在資料 Lake Analytics 中，在目錄或目錄專案的存取控制清單 (ACL) 中，新增或修改 (ACE) 中的專案。</span><span class="sxs-lookup"><span data-stu-id="d792a-116">The **Set-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet adds or modifies an entry (ACE) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="d792a-117">示例</span><span class="sxs-lookup"><span data-stu-id="d792a-117">EXAMPLES</span></span>

### <span data-ttu-id="d792a-118">範例1：修改目錄的使用者許可權</span><span class="sxs-lookup"><span data-stu-id="d792a-118">Example 1: Modify user permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="d792a-119">這個命令會將 [Patti] 的目錄 ACE 完整地修改為擁有讀取權限。</span><span class="sxs-lookup"><span data-stu-id="d792a-119">This command modifies the catalog ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="d792a-120">範例2：修改資料庫的使用者許可權</span><span class="sxs-lookup"><span data-stu-id="d792a-120">Example 2: Modify user Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="d792a-121">這個命令會將 [Patti] 的資料庫 ACE 完整地修改為擁有讀取權限。</span><span class="sxs-lookup"><span data-stu-id="d792a-121">This command modifies the database ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="d792a-122">範例3：修改目錄的其他許可權</span><span class="sxs-lookup"><span data-stu-id="d792a-122">Example 3: Modify other permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="d792a-123">這個命令會修改目錄 ACE，讓其他擁有讀取權限。</span><span class="sxs-lookup"><span data-stu-id="d792a-123">This command modifies the catalog ACE for other to have read permissions.</span></span>

### <span data-ttu-id="d792a-124">範例4：修改資料庫的其他許可權</span><span class="sxs-lookup"><span data-stu-id="d792a-124">Example 4: Modify other Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

### <span data-ttu-id="d792a-125">範例5：修改目錄的使用者擁有者許可權</span><span class="sxs-lookup"><span data-stu-id="d792a-125">Example 5: Modify user owner permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -Permissions Read

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="d792a-126">這個命令會將帳戶的擁有者許可權設定為 [已讀取]。</span><span class="sxs-lookup"><span data-stu-id="d792a-126">This command sets the owner permission for the account to Read.</span></span>

### <span data-ttu-id="d792a-127">範例6：修改資料庫的使用者擁有者許可權</span><span class="sxs-lookup"><span data-stu-id="d792a-127">Example 6: Modify user owner Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName" -Permissions Read

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="d792a-128">這個命令會將資料庫的擁有者許可權設定為 [讀取]。</span><span class="sxs-lookup"><span data-stu-id="d792a-128">This command sets the owner permission for the database to Read.</span></span>

## <span data-ttu-id="d792a-129">參數</span><span class="sxs-lookup"><span data-stu-id="d792a-129">PARAMETERS</span></span>

### <span data-ttu-id="d792a-130">-帳戶</span><span class="sxs-lookup"><span data-stu-id="d792a-130">-Account</span></span>
<span data-ttu-id="d792a-131">指定 Data Lake Analytics 帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d792a-131">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d792a-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d792a-132">-DefaultProfile</span></span>
<span data-ttu-id="d792a-133">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d792a-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d792a-134">-群組</span><span class="sxs-lookup"><span data-stu-id="d792a-134">-Group</span></span>
<span data-ttu-id="d792a-135">設定群組的目錄 ACL 專案。</span><span class="sxs-lookup"><span data-stu-id="d792a-135">Set ACL entry of catalog for group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForGroup, SetCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d792a-136">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="d792a-136">-GroupOwner</span></span>
<span data-ttu-id="d792a-137">設定群組擁有者的目錄 ACL 專案。</span><span class="sxs-lookup"><span data-stu-id="d792a-137">Set ACL entry of catalog for group owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForGroupOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d792a-138">-ItemType</span><span class="sxs-lookup"><span data-stu-id="d792a-138">-ItemType</span></span>
<span data-ttu-id="d792a-139">指定 (s) 的目錄或目錄專案類型。</span><span class="sxs-lookup"><span data-stu-id="d792a-139">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="d792a-140">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d792a-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d792a-141">類別</span><span class="sxs-lookup"><span data-stu-id="d792a-141">Catalog</span></span>
- <span data-ttu-id="d792a-142">資料</span><span class="sxs-lookup"><span data-stu-id="d792a-142">Database</span></span>

```yaml
Type: System.String
Parameter Sets: SetCatalogItemAclEntryForUser, SetCatalogItemAclEntryForGroup, SetCatalogItemAclEntryForOther, SetCatalogItemAclEntryForUserOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d792a-143">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d792a-143">-ObjectId</span></span>
<span data-ttu-id="d792a-144">要設定的使用者身分識別。</span><span class="sxs-lookup"><span data-stu-id="d792a-144">The identity of the user to set.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SetCatalogAclEntryForUser, SetCatalogItemAclEntryForUser, SetCatalogAclEntryForGroup, SetCatalogItemAclEntryForGroup
Aliases: Id, UserId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d792a-145">-其他</span><span class="sxs-lookup"><span data-stu-id="d792a-145">-Other</span></span>
<span data-ttu-id="d792a-146">設定 [其他] 類別的 [ACL] 專案。</span><span class="sxs-lookup"><span data-stu-id="d792a-146">Set ACL entry of catalog for other.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForOther, SetCatalogItemAclEntryForOther
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d792a-147">-Path</span><span class="sxs-lookup"><span data-stu-id="d792a-147">-Path</span></span>
<span data-ttu-id="d792a-148">指定目錄或目錄專案的資料 Lake Analytics 路徑。</span><span class="sxs-lookup"><span data-stu-id="d792a-148">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="d792a-149">路徑的各個部分應以句點 ( ) 。</span><span class="sxs-lookup"><span data-stu-id="d792a-149">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: SetCatalogItemAclEntryForUser, SetCatalogItemAclEntryForGroup, SetCatalogItemAclEntryForOther, SetCatalogItemAclEntryForUserOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d792a-150">-許可權</span><span class="sxs-lookup"><span data-stu-id="d792a-150">-Permissions</span></span>
<span data-ttu-id="d792a-151">指定 ACE 的許可權。</span><span class="sxs-lookup"><span data-stu-id="d792a-151">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="d792a-152">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d792a-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d792a-153">所有</span><span class="sxs-lookup"><span data-stu-id="d792a-153">None</span></span>
- <span data-ttu-id="d792a-154">查看</span><span class="sxs-lookup"><span data-stu-id="d792a-154">Read</span></span>
- <span data-ttu-id="d792a-155">讀</span><span class="sxs-lookup"><span data-stu-id="d792a-155">ReadWrite</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, ReadWrite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d792a-156">-使用者</span><span class="sxs-lookup"><span data-stu-id="d792a-156">-User</span></span>
<span data-ttu-id="d792a-157">為使用者設定目錄的 ACL 專案。</span><span class="sxs-lookup"><span data-stu-id="d792a-157">Set ACL entry of catalog for user.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForUser, SetCatalogItemAclEntryForUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d792a-158">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="d792a-158">-UserOwner</span></span>
<span data-ttu-id="d792a-159">為使用者擁有者設定目錄的 ACL 專案。</span><span class="sxs-lookup"><span data-stu-id="d792a-159">Set ACL entry of catalog for user owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForUserOwner, SetCatalogItemAclEntryForUserOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d792a-160">-確認</span><span class="sxs-lookup"><span data-stu-id="d792a-160">-Confirm</span></span>
<span data-ttu-id="d792a-161">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d792a-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d792a-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d792a-162">-WhatIf</span></span>
<span data-ttu-id="d792a-163">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d792a-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d792a-164">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d792a-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d792a-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d792a-165">CommonParameters</span></span>
<span data-ttu-id="d792a-166">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d792a-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d792a-167">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d792a-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d792a-168">輸入</span><span class="sxs-lookup"><span data-stu-id="d792a-168">INPUTS</span></span>

### <span data-ttu-id="d792a-169">System.object</span><span class="sxs-lookup"><span data-stu-id="d792a-169">System.String</span></span>

### <span data-ttu-id="d792a-170">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="d792a-170">System.Guid</span></span>

### <span data-ttu-id="d792a-171">CatalogPathInstance 中的 DataLakeAnalytics。</span><span class="sxs-lookup"><span data-stu-id="d792a-171">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

### <span data-ttu-id="d792a-172">DataLakeAnalyticsEnums + PermissionType （DataLakeAnalytics）。</span><span class="sxs-lookup"><span data-stu-id="d792a-172">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType</span></span>

## <span data-ttu-id="d792a-173">輸出</span><span class="sxs-lookup"><span data-stu-id="d792a-173">OUTPUTS</span></span>

### <span data-ttu-id="d792a-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="d792a-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="d792a-175">筆記</span><span class="sxs-lookup"><span data-stu-id="d792a-175">NOTES</span></span>

## <span data-ttu-id="d792a-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="d792a-176">RELATED LINKS</span></span>

[<span data-ttu-id="d792a-177">AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d792a-177">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="d792a-178">移除-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="d792a-178">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="d792a-179">U-SQL 現已提供資料庫層級存取控制</span><span class="sxs-lookup"><span data-stu-id="d792a-179">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
ms.openlocfilehash: e26d8aa68fd7ffcbab45073b845352feae83aea5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136649"
---
# <span data-ttu-id="49861-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="49861-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="49861-102">摘要</span><span class="sxs-lookup"><span data-stu-id="49861-102">SYNOPSIS</span></span>
<span data-ttu-id="49861-103">針對指定的受管理實例新增透明的資料加密憑證</span><span class="sxs-lookup"><span data-stu-id="49861-103">Adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="49861-104">句法</span><span class="sxs-lookup"><span data-stu-id="49861-104">SYNTAX</span></span>

```
Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ManagedInstanceName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49861-105">說明</span><span class="sxs-lookup"><span data-stu-id="49861-105">DESCRIPTION</span></span>
<span data-ttu-id="49861-106">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate 為指定的受管理實例新增透明的資料加密憑證</span><span class="sxs-lookup"><span data-stu-id="49861-106">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="49861-107">示例</span><span class="sxs-lookup"><span data-stu-id="49861-107">EXAMPLES</span></span>

### <span data-ttu-id="49861-108">範例1</span><span class="sxs-lookup"><span data-stu-id="49861-108">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ManagedInstanceName "YourManagedInstanceName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

## <span data-ttu-id="49861-109">參數</span><span class="sxs-lookup"><span data-stu-id="49861-109">PARAMETERS</span></span>

### <span data-ttu-id="49861-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49861-110">-DefaultProfile</span></span>
<span data-ttu-id="49861-111">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="49861-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49861-112">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="49861-112">-ManagedInstanceName</span></span>
<span data-ttu-id="49861-113">受管理的實例名稱</span><span class="sxs-lookup"><span data-stu-id="49861-113">The managed instance name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49861-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49861-114">-PassThru</span></span>
<span data-ttu-id="49861-115">成功執行時，會傳回已新增的憑證物件。</span><span class="sxs-lookup"><span data-stu-id="49861-115">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="49861-116">-Password</span><span class="sxs-lookup"><span data-stu-id="49861-116">-Password</span></span>
<span data-ttu-id="49861-117">透明資料加密憑證的密碼</span><span class="sxs-lookup"><span data-stu-id="49861-117">The Password for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49861-118">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="49861-118">-PrivateBlob</span></span>
<span data-ttu-id="49861-119">透明資料加密憑證的專用 blob</span><span class="sxs-lookup"><span data-stu-id="49861-119">The Private blob for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49861-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49861-120">-ResourceGroupName</span></span>
<span data-ttu-id="49861-121">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="49861-121">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49861-122">-確認</span><span class="sxs-lookup"><span data-stu-id="49861-122">-Confirm</span></span>
<span data-ttu-id="49861-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="49861-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49861-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49861-124">-WhatIf</span></span>
<span data-ttu-id="49861-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="49861-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49861-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="49861-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49861-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49861-127">CommonParameters</span></span>
<span data-ttu-id="49861-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="49861-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49861-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="49861-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49861-130">輸入</span><span class="sxs-lookup"><span data-stu-id="49861-130">INPUTS</span></span>

### <span data-ttu-id="49861-131">所有</span><span class="sxs-lookup"><span data-stu-id="49861-131">None</span></span>

## <span data-ttu-id="49861-132">輸出</span><span class="sxs-lookup"><span data-stu-id="49861-132">OUTPUTS</span></span>

### <span data-ttu-id="49861-133">System.object</span><span class="sxs-lookup"><span data-stu-id="49861-133">System.Boolean</span></span>

## <span data-ttu-id="49861-134">筆記</span><span class="sxs-lookup"><span data-stu-id="49861-134">NOTES</span></span>

## <span data-ttu-id="49861-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="49861-135">RELATED LINKS</span></span>

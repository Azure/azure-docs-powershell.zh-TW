---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationAzureActiveDirectoryApp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationAzureActiveDirectoryApp.md
ms.openlocfilehash: 8eec47c703290047b51ce38e97391500a9f27d74
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136323"
---
# <span data-ttu-id="11f03-101">New-AzDataMigrationAzureActiveDirectoryApp</span><span class="sxs-lookup"><span data-stu-id="11f03-101">New-AzDataMigrationAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="11f03-102">摘要</span><span class="sxs-lookup"><span data-stu-id="11f03-102">SYNOPSIS</span></span>
<span data-ttu-id="11f03-103">建立新的實例 DataMigration Azure ActiveDirectory 應用程式詳細資料。</span><span class="sxs-lookup"><span data-stu-id="11f03-103">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="11f03-104">句法</span><span class="sxs-lookup"><span data-stu-id="11f03-104">SYNTAX</span></span>

```
New-AzDataMigrationAzureActiveDirectoryApp -ApplicationId <String> -AppKey <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11f03-105">說明</span><span class="sxs-lookup"><span data-stu-id="11f03-105">DESCRIPTION</span></span>
<span data-ttu-id="11f03-106">建立新的實例 DataMigration Azure ActiveDirectory 應用程式詳細資料。</span><span class="sxs-lookup"><span data-stu-id="11f03-106">Create a new instance DataMigration Azure ActiveDirectory Application details.</span></span>

## <span data-ttu-id="11f03-107">示例</span><span class="sxs-lookup"><span data-stu-id="11f03-107">EXAMPLES</span></span>

### <span data-ttu-id="11f03-108">範例1</span><span class="sxs-lookup"><span data-stu-id="11f03-108">Example 1</span></span>
```powershell
PS C:\> $secpasswd = ConvertTo-SecureString "Your Secret Key Here" -AsPlainText -Force
C:\> New-AzDmsAadApp -ApplicationId "Your AppId/Service Principal ID here" -AppKey $secpasswd
```
<span data-ttu-id="11f03-109">[ApplicationId：「您的 AppId/服務主體識別碼] AppKey： SecureString TenantId： "租使用者識別碼"</span><span class="sxs-lookup"><span data-stu-id="11f03-109">ApplicationId : "Your AppId/Service Principal Id here" AppKey        : System.Security.SecureString TenantId      : "Tenant Id"</span></span>

## <span data-ttu-id="11f03-110">參數</span><span class="sxs-lookup"><span data-stu-id="11f03-110">PARAMETERS</span></span>

### <span data-ttu-id="11f03-111">-AppKey</span><span class="sxs-lookup"><span data-stu-id="11f03-111">-AppKey</span></span>
<span data-ttu-id="11f03-112">Azure Active Directory 金鑰</span><span class="sxs-lookup"><span data-stu-id="11f03-112">Azure Active Directory Key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: Key

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f03-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="11f03-113">-ApplicationId</span></span>
<span data-ttu-id="11f03-114">Azure Active Directory 應用程式識別碼</span><span class="sxs-lookup"><span data-stu-id="11f03-114">Azure Active Directory Application Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11f03-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11f03-115">-DefaultProfile</span></span>
<span data-ttu-id="11f03-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="11f03-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11f03-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11f03-117">CommonParameters</span></span>
<span data-ttu-id="11f03-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="11f03-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="11f03-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="11f03-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11f03-120">輸入</span><span class="sxs-lookup"><span data-stu-id="11f03-120">INPUTS</span></span>

### <span data-ttu-id="11f03-121">所有</span><span class="sxs-lookup"><span data-stu-id="11f03-121">None</span></span>

## <span data-ttu-id="11f03-122">輸出</span><span class="sxs-lookup"><span data-stu-id="11f03-122">OUTPUTS</span></span>

### <span data-ttu-id="11f03-123">PSAzureActiveDirectoryApp 中的 DataMigration。</span><span class="sxs-lookup"><span data-stu-id="11f03-123">Microsoft.Azure.Commands.DataMigration.Models.PSAzureActiveDirectoryApp</span></span>

## <span data-ttu-id="11f03-124">筆記</span><span class="sxs-lookup"><span data-stu-id="11f03-124">NOTES</span></span>

## <span data-ttu-id="11f03-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="11f03-125">RELATED LINKS</span></span>
